### Version Pragma

Source files can (and should) be annotated with a so-called version pragma to reject being compiled with future compiler versions that might introduce incompatible changes.

The version pragma is used as follows:

```
pragma solidity ^0.4.18;
```

Such a source file will not compile with a compiler earlier than version 0.4.0 and it will also not work on a compiler starting from version 0.5.0 (this second condition is added by using ^). The idea behind this is that there will be no breaking changes until version 0.5.0, so we can always be sure that our code will compile the way we intended it to. We do not fix the exact version of the compiler, so that bugfix releases are still possible.

### Importing other Source Files

http://solidity.readthedocs.io/en/develop/layout-of-source-files.html#importing-other-source-files

### Comments

Single-line comments (`//)` and multi-line comments (`/*...*/`) are possible.

```
// This is a single-line comment.

/*
This is a
multi-line comment.
*/
```

### Structure of a Contract

#### State Variables

State variables are values which are permanently stored in contract storage.

```
pragma solidity ^0.4.0;

contract SimpleStorage {
    uint storedData; // State variable
    // ...
}
```
#### Functions

Functions are the executable units of code within a contract.

Function types are notated as follows:

```
function (<parameter types>) {internal|external} [pure|constant|view|payable] [returns (<return types>)]
```

Example:

```
pragma solidity ^0.4.0;

contract SimpleAuction {
    function bid() public payable { // Function
        // ...
    }
}
```

#### Function Modifiers

Function modifiers can be used to amend the semantics of functions in a declarative way.

```
pragma solidity ^0.4.11;

contract Purchase {
    address public seller;

    modifier onlySeller() { // Modifier
        require(msg.sender == seller);
        _;
    }

    function abort() public onlySeller { // Modifier usage
        // ...
    }
}
```

#### Events

Events are convenience interfaces with the EVM logging facilities.

```
pragma solidity ^0.4.0;

contract SimpleAuction {
    event HighestBidIncreased(address bidder, uint amount); // Event

    function bid() public payable {
        // ...
        HighestBidIncreased(msg.sender, msg.value); // Triggering event
    }
}
```

#### Struct Types

Structs are custom defined types that can group several variables.

```
pragma solidity ^0.4.0;

contract Ballot {
    struct Voter { // Struct
        uint weight;
        bool voted;
        address delegate;
        uint vote;
    }
}
```

#### Enum Types

Enums can be used to create custom types with a finite set of values.

```
pragma solidity ^0.4.0;

contract Purchase {
    enum State { Created, Locked, Inactive } // Enum
}
```

### Types

#### Value Types

- bool: The possible values are constants true and false.

- int / uint: Signed and unsigned integers of various sizes. Keywords uint8 to uint256 in steps of 8 (unsigned of 8 up to 256 bits) and int8 to int256. uint and int are aliases for uint256 and int256, respectively.

- address: Holds a 20 byte value (size of an Ethereum address). Address types also have members and serve as a base for all contracts.

- balance and transfer

It is possible to query the balance of an address using the property balance and to send Ether (in units of wei) to an address using the transfer function:

```
address x = 0x123;
address myAddress = this;
if (x.balance < 10 && myAddress.balance >= 10) x.transfer(10);
```

- send

Send is the low-level counterpart of transfer. If the execution fails, the current contract will not stop with an exception, but send will return false.

#### Reference Types

The default for function parameters (including return parameters) is `memory`, the default for local variables is `storage` and the location is forced to storage for state variables (obviously).


#### Creating Contracts via new

A contract can create a new contract using the new keyword. The full code of the contract being created has to be known in advance, so recursive creation-dependencies are not possible.

```
pragma solidity ^0.4.0;

contract D {
    uint x;
    function D(uint a) public payable {
        x = a;
    }
}

contract C {
    D d = new D(4); // will be executed as part of C's constructor

    function createD(uint arg) public {
        D newD = new D(arg);
    }

    function createAndEndowD(uint arg, uint amount) public payable {
        // Send ether along with the creation
        D newD = (new D).value(amount)(arg);
    }
}
```
---
description: Algorithm Complexity
keywords: algorithm, complexity
title: Algorithm Complexity
---

## Algorithm Complexity

## Table of common time complexities

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th><a href="https://en.wikipedia.org/wiki/Complexity_class" title="Complexity class">Complexity class</a></th>
      <th>Running time (<i>T</i>(<i>n</i>))</th>
      <th>Examples of running times</th>
      <th>Example algorithms</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>constant time</td>
      <td></td>
      <td><i>O</i>(1)</td>
      <td>10</td>
      <td>Determining if an integer (represented in binary) is even or odd</td>
    </tr>
    <tr>
      <td><a href="https://en.wikipedia.org/wiki/Inverse_Ackermann_function" title="Inverse Ackermann function">inverse Ackermann</a> time</td>
      <td></td>
      <td><i>O</i>(<i>α</i>(<i>n</i>))</td>
      <td></td>
      <td><a href="https://en.wikipedia.org/wiki/Amortized_time" title="Amortized time">Amortized time</a> per operation using a <a href="https://en.wikipedia.org/wiki/Disjoint_set_data_structure" title="Disjoint set data structure">disjoint set</a></td>
    </tr>
    <tr>
      <td><a href="https://en.wikipedia.org/wiki/Iterated_logarithm" title="Iterated logarithm">iterated logarithmic</a> time</td>
      <td></td>
      <td><i>O</i>(<a href="https://en.wikipedia.org/wiki/Iterated_logarithm" title="Iterated logarithm">log<span style="vertical-align: 10%">*</span></a>&nbsp;<i>n</i>)</td>
      <td></td>
      <td><a href="https://en.wikipedia.org/wiki/Cole-Vishkin_algorithm" title="Cole-Vishkin algorithm">Distributed coloring of cycles</a></td>
    </tr>
    <tr>
      <td>log-logarithmic</td>
      <td></td>
      <td><i>O</i>(log log <i>n</i>)</td>
      <td></td>
      <td>Amortized time per operation using a bounded <a href="https://en.wikipedia.org/wiki/Priority_queue" title="Priority queue">priority queue</a><sup id="cite_ref-2" class="reference"><a href="#cite_note-2">[2]</a></sup></td>
    </tr>
    <tr>
      <td>logarithmic time</td>
      <td><a href="https://en.wikipedia.org/wiki/DLOGTIME" title="DLOGTIME">DLOGTIME</a></td>
      <td><i>O</i>(log&nbsp;<i>n</i>)</td>
      <td>log&nbsp;<i>n</i>, log(<i>n</i><sup>2</sup>)</td>
      <td><a href="https://en.wikipedia.org/wiki/Binary_search" title="Binary search">Binary search</a></td>
    </tr>
    <tr>
      <td>polylogarithmic time</td>
      <td></td>
      <td>poly(log&nbsp;<i>n</i>)</td>
      <td>(log&nbsp;<i>n</i>)<sup>2</sup></td>
      <td></td>
    </tr>
    <tr>
      <td>fractional power</td>
      <td></td>
      <td><span class="texhtml"><i>O</i>(<i>n</i><sup>c</sup>)</span> where <span class="texhtml">0 &lt; c &lt; 1</span></td>
      <td><i>n</i><sup>1/2</sup>, <i>n</i><sup>2/3</sup></td>
      <td>Searching in a <a href="https://en.wikipedia.org/wiki/Kd-tree" class="mw-redirect" title="Kd-tree">kd-tree</a></td>
    </tr>
    <tr>
      <td>linear time</td>
      <td></td>
      <td><i>O</i>(<i>n</i>)</td>
      <td><i>n</i></td>
      <td>Finding the smallest or largest item in an unsorted <a href="https://en.wikipedia.org/wiki/Array_data_structure" title="Array data structure">array</a></td>
    </tr>
    <tr>
      <td>"n log star n" time</td>
      <td></td>
      <td><i>O</i>(<i>n</i>&nbsp;<a href="https://en.wikipedia.org/wiki/Iterated_logarithm" title="Iterated logarithm">log<span style="vertical-align: 10%">*</span></a>&nbsp;<i>n</i>)</td>
      <td></td>
      <td><a href="https://en.wikipedia.org/wiki/Raimund_Seidel" title="Raimund Seidel">Seidel</a>'s <a href="https://en.wikipedia.org/wiki/Polygon_triangulation" title="Polygon triangulation">polygon triangulation</a> algorithm.</td>
    </tr>
    <tr>
      <td>quasilinear time</td>
      <td></td>
      <td><i>O</i>(<i>n</i>&nbsp;log&nbsp;<i>n</i>)</td>
      <td><i>n</i>&nbsp;log&nbsp;<i>n</i>, log <i>n</i>!</td>
      <td>Fastest possible <a href="https://en.wikipedia.org/wiki/Comparison_sort" title="Comparison sort">comparison sort</a>; <a href="https://en.wikipedia.org/wiki/Fast_Fourier_transform" title="Fast Fourier transform">Fast Fourier transform</a>.</td>
    </tr>
    <tr>
      <td>quadratic time</td>
      <td></td>
      <td><i>O</i>(<i>n</i><sup>2</sup>)</td>
      <td><i>n</i><sup>2</sup></td>
      <td><a href="https://en.wikipedia.org/wiki/Bubble_sort" title="Bubble sort">Bubble sort</a>; <a href="https://en.wikipedia.org/wiki/Insertion_sort" title="Insertion sort">Insertion sort</a>; <a href="https://en.wikipedia.org/wiki/Convolution_theorem" title="Convolution theorem">Direct convolution</a></td>
    </tr>
    <tr>
      <td>cubic time</td>
      <td></td>
      <td><i>O</i>(<i>n</i><sup>3</sup>)</td>
      <td><i>n</i><sup>3</sup></td>
      <td>Naive multiplication of two <i>n</i>×<i>n</i> matrices. Calculating <a href="https://en.wikipedia.org/wiki/Partial_correlation" title="Partial correlation">partial correlation</a>.</td>
    </tr>
    <tr>
      <td>polynomial time</td>
      <td><a href="https://en.wikipedia.org/wiki/P_(complexity)" title="P (complexity)">P</a></td>
      <td>2<sup><i>O</i>(log&nbsp;<i>n</i>)</sup> = poly(<i>n</i>)</td>
      <td><i>n</i>, <i>n</i>&nbsp;log&nbsp;<i>n</i>, <i>n</i><sup>10</sup></td>
      <td><a href="https://en.wikipedia.org/wiki/Karmarkar%27s_algorithm" title="Karmarkar's algorithm">Karmarkar's algorithm</a> for <a href="https://en.wikipedia.org/wiki/Linear_programming" title="Linear programming">linear programming</a>; <a href="https://en.wikipedia.org/wiki/AKS_primality_test" title="AKS primality test">AKS primality test</a></td>
    </tr>
    <tr>
      <td>quasi-polynomial time</td>
      <td>QP</td>
      <td>2<sup>poly(log&nbsp;<i>n</i>)</sup></td>
      <td><i>n</i><sup>log&nbsp;log&nbsp;<i>n</i></sup>, <i>n</i><sup>log&nbsp;<i>n</i></sup></td>
      <td>Best-known O(log<sup>2</sup> <i>n</i>)-<a href="https://en.wikipedia.org/wiki/Approximation_algorithm" title="Approximation algorithm">approximation algorithm</a> for the directed <a href="https://en.wikipedia.org/wiki/Steiner_tree_problem" title="Steiner tree problem">Steiner tree problem</a>.</td>
    </tr>
    <tr>
      <td>sub-exponential time
        <br> (first definition)
      </td>
      <td>SUBEXP</td>
      <td><i>O</i>(2<sup><i>n</i><sup><i>ε</i></sup></sup>) for all <i>ε</i>&nbsp;&gt;&nbsp;0</td>
      <td><i>O</i>(2<sup>log <i>n</i><sup>log log <i>n</i></sup></sup>)</td>
      <td>Assuming complexity theoretic conjectures, <a href="https://en.wikipedia.org/wiki/Bounded-error_probabilistic_polynomial" class="mw-redirect" title="Bounded-error probabilistic polynomial">BPP</a> is contained in SUBEXP.<sup id="cite_ref-bpp_3-0" class="reference"><a href="#cite_note-bpp-3">[3]</a></sup></td>
    </tr>
    <tr>
      <td>sub-exponential time
        <br> (second definition)
      </td>
      <td></td>
      <td>2<sup><i>o</i>(<i>n</i>)</sup></td>
      <td>2<sup><i>n</i><sup>1/3</sup></sup>
      </td>
      <td>Best-known algorithm for <a href="https://en.wikipedia.org/wiki/Integer_factorization" title="Integer factorization">integer factorization</a> and <a href="https://en.wikipedia.org/wiki/Graph_isomorphism_problem" title="Graph isomorphism problem">graph isomorphism</a></td>
    </tr>
    <tr>
      <td>exponential time
        <br> (with linear exponent)
      </td>
      <td><a href="https://en.wikipedia.org/wiki/E_(complexity)" title="E (complexity)">E</a></td>
      <td>2<sup><i>O</i>(<i>n</i>)</sup></td>
      <td>1.1<sup><i>n</i></sup>, 10<sup><i>n</i></sup></td>
      <td>Solving the <a href="https://en.wikipedia.org/wiki/Traveling_salesman_problem" class="mw-redirect" title="Traveling salesman problem">traveling salesman problem</a> using <a href="https://en.wikipedia.org/wiki/Dynamic_programming" title="Dynamic programming">dynamic programming</a></td>
    </tr>
    <tr>
      <td>exponential time</td>
      <td><a href="https://en.wikipedia.org/wiki/EXPTIME" title="EXPTIME">EXPTIME</a></td>
      <td>2<sup>poly(<i>n</i>)</sup></td>
      <td>2<sup><i>n</i></sup>, 2<sup><i>n</i><sup>2</sup></sup>
      </td>
      <td>Solving <a href="https://en.wikipedia.org/wiki/Matrix_chain_multiplication" title="Matrix chain multiplication">matrix chain multiplication</a> via <a href="https://en.wikipedia.org/wiki/Brute-force_search" title="Brute-force search">brute-force search</a></td>
    </tr>
    <tr>
      <td>factorial time</td>
      <td></td>
      <td><i>O</i>(<i>n</i>!)</td>
      <td><i>n</i>!</td>
      <td>Solving the <a href="https://en.wikipedia.org/wiki/Travelling_salesman_problem" title="Travelling salesman problem">traveling salesman problem</a> via <a href="https://en.wikipedia.org/wiki/Brute-force_search" title="Brute-force search">brute-force search</a></td>
    </tr>
    <tr>
      <td>double exponential time</td>
      <td><a href="https://en.wikipedia.org/wiki/2-EXPTIME" title="2-EXPTIME">2-EXPTIME</a></td>
      <td>2<sup>2<sup>poly(<i>n</i>)</sup></sup>
      </td>
      <td>2<sup>2<sup><i>n</i></sup></sup>
      </td>
      <td>Deciding the truth of a given statement in <a href="https://en.wikipedia.org/wiki/Presburger_arithmetic" title="Presburger arithmetic">Presburger arithmetic</a></td>
    </tr>
  </tbody>
</table>

## Resources

- [https://en.wikipedia.org/wiki/Time_complexity](https://en.wikipedia.org/wiki/Time_complexity)

- [http://bigocheatsheet.com/](http://bigocheatsheet.com/)

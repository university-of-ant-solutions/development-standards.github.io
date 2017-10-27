---
description: If I was to build a website from scratch in 2017
keywords: research, website, scratch
title: If I was to build a website from scratch in 2017
---

## If I were to build a website right now from scratch, what language and tools would you use?

For a release in 2018AD:

A containerized back-end service mesh managed by Kubernetes and wired together using Istio.

Services implemented primarily in Python, with Go in performance-critical points. Internal communication using gRPC. External communication using REST and GraphQL, as appropriate.

Scaleout queues using Kafka. Offline and stream processing using Spark. Persistent caching storage in Cassandra, and relational data using Postgres, with text indexing using ElasticSearch.

Front-end written in TypeScript, on top of React/Redux, all packaged using Webpack and deployed to CDN using jenkins, with NGINX caching proxy servers.

Rollout using Salt. Log aggregation using Sumo, and Graphite for metrics.

We could probably go on, but the above represents close to the state of the current art, without going way off the rails with Scala/Clojure, etc.

And you wonder why software engineers are well-paid these days. ;)

The above is pretty close to what we’re working on these days, actually, although we do have some complex distributed engines written in Scala, as well as a bit more “variety” on the front-end stack, and a lot more JavaScript on the back-end.

When your “website” lives in the real world and you’re massively successful, the website’s infrastructure experiences explosive growth. The above stack is designed to assist in managing all that. As usual, though, it’s the processes and architecture that make the big difference, not the tech, per se.

The above stack is also designed to solve the problem of developing, deploying, and operating a massive, complex system. Simpler systems can benefit from much simpler stacks. For example, a serverless setup consisting of AWS lambda, with content stored in S3/, and data stored in DynamoDB could be a choice for a startup trying to get to an MVP quickly at minimal cost, but with high scalability and resilience.

## Resources

- [https://www.quora.com/If-you-were-to-build-a-website-right-now-from-scratch-what-language-and-tools-would-you-use](https://www.quora.com/If-you-were-to-build-a-website-right-now-from-scratch-what-language-and-tools-would-you-use)

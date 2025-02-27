---
title: Chainhooks
---

## Overview

Chainhooks are a powerful feature that enables you to automatically trigger an action based upon a predicate event occurring. Adhering to an event-based architecture, chainhooks allow you to pre-determine an underlying set of events that, when triggered, set into motion a logical series of follow-on steps and actions to address the specific event that was triggered.

*Topics covered in this guide*:

* [Chainhooks design](#design)
* [Use chainhooks](#using-chainhooks)
* [References](#references)

## Design

Chainhooks were designed with a very specific set of requirements and limitations to make them easy to work with in a development environment. These constraints include portability and performance.

- portability and performance

Hiro designed the event observer as a library, choosing to embed the library in Clarinet so you can run it on your local machine. You may also execute the library on the server side and then propagate these HTTP events to your other components.

- correctness

Due to the fact that blockchains can be forked—and some period of uncertainty may arise as to which chain tip asserts itself as the canonical chain—there are challenges to guaranteeing the validity of a triggered predicate. There are many different ways you can end up with a state slightly differing from the canonical state, which is why correctness is an inherent limitation of chainhooks. 

## Using chainhooks

The chainhook-event-observer is a sidecar program that observes a given stacks node. Although this layer is open source, Hiro is currently developing a managed version. In the meantime, you are encouraged to run your own stacks node with your own chainhook-event observer.

In terms of the deployment lifecycle, you can begin using chainhooks locally, using the latest version of Clarinet, or you may deploy chainhooks in your own environment.

**Note:** If you choose to deploy chainhooks in your own environment, please be aware that you are responsible for your own deployment instead of relying on Hiro's default deployment architecture.

## References

For a more detailed discussion of Chainhooks and how you can use them in your workflows, please see the following resources:

- [Meet 4 New Features in Clarinet](https://www.hiro.so/blog/meet-4-new-features-in-clarinet) blog post.

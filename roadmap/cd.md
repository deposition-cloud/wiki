---
title: Continuous Delivery
description: CI/CD
img: first-blog-post.jpg
alt: my first blog post
author:
  name: Paul Cuciureanu
  bio: Freewilling Hacker
  image: http://lorempixel.com/g/400/200/
---
# Meta

2 clusters: `live` and `omega`

A `live` cluster can service multiple online communities, some of which may use shared services, e.g.: ingress controllers, databases(?). This is an app-level decision.

To pre-empt the rise of ML-aware deployments, let's focus on the [A/B testing deployment pattern](https://cloud.google.com/solutions/application-deployment-and-testing-strategies#choosing_the_right_strategy) which should come out of the box.

We'll have A/B capabilities on `live`, however, we can also think of `live` and `omega` as a kind of cluster-level "A/B" test. The concern we need to address is downtime during a Kubernetes version upgrade, as well as a major OS upgrade.

### `live`

The first environment where we continuous deliver into. If we mess up, great: roll-back and deploy to omega to debug.

This is backwards to industry best practices where the goal is to not affect the user experience.

For us, the user experience _is the cloud_ improving and serving us better, and our risk profile is not the same as your average iPhone user. We have:
- backups
- deep technical knowledge
- troubleshooting aptitude

This is my personal cloud, I am the creator, user, and maintainer of it. It's much like taking care of and designing my living room. I can match furniture sure, but the overall aesthetic is my responsability, as I live it. As my life circumstance changes, so does my livingroom (new kid, friends over), and now, so does my personal cloud.

### `omega`

Why "omega"? It's not alpha nor beta (both of which represent a batch of changes), rather, `omega` might literally be just 1 commit ahead of `live`.

`omega`, as a prod-paralel environment, provides us a safe space to investigate heisenbugs we saw fail the `live` cluster; we can now contain the blast radius and can think deeply unencumberd.

Nonetheless, we always first deploy to `live`, like with [Dark](https://darklang.com/).

## Qualities

1. Evolvable: `live` and `omega` should operate like a blue/green cluster setup, make it easy to revert `live` traffic to `omega` (which should be operating under a near-real-time data backup, and so nearly 100% useful to us, the end users)
1. Upgradeable
1. Temp multi-tenant: goal is to constantly decentralize, however, we can use existing infra to prototype other communities deposited clouds
1. Scale-free integration: A/B deploy apps to namespaces, A/B cluster services to `live`/`omega`, operating systems to VMs. (A/(A/(A/B)))

## To Dos

- [ ] Plan a Pulumi approach with a `-omega` flag to shift the IaC to `omega`

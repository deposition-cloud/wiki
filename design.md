---
title: Design
description: Choices with long-term impact
img: first-blog-post.jpg
alt: my first blog post
author:
  name: Paul Cuciureanu
  bio: Hacker
  image: http://lorempixel.com/g/400/200/
---
# Design

Integrating an evolving system is difficult.

We need to be flexible, things will break. We'll get hacked, or a leak some data due to a software bug at any layer of the stack.

## Abstraction Layers

Think in holistically in layers, making an improvement in one category will affect the other layers. Start over when you notice that happen.

1. Social Data
   1. Shareable
   2. Anonymity
2. Personal Data
   1. Encryption
   2. Backup
3. Applications
4. Security and Identity
   1. TLS
   2. HTTPS
   3. GPG
5. Container Orchestration
   1. MicroK8s
6. Operating Systems
   1. Ubuntu
   2. Windows
7. Network
   1. LAN
   2. ISP
   3. Firewall
8. Hardware
   1. Compute
   2. IoT around the house
   3. Hardware Wallet

Because the technological stack is so incredibly complex, we need good heuristics to help us make pragmatic decisions.

## Qualities

We can look at the history of commits to evaluate progress against these interests.

Our goal in spelling these high level systemic properties out is to understand the tradeoffs we're making in code and social behaviour.

1. Usefulness over Privacy
   1. We're willing to explore new tools to understand how might we integrate them to make the whole system more[^1]:
      1. Credible - shows correct information
      2. Desirable - feels and looks good
      3. Accessible - context aware
      4. Usable - it just works
      5. Findable - searchable
      6. Useful - helps solve real problems we have
    Notice when we over invest in any one of these dimensions and compensate; re: layered thinking. Remember that early decision will have long lasting consequences.
      Since code is easy to change, we can rebuild the entire stack when we realize we've made a mistake.
2. Public over Protected
   1. We need feedback from outside our head, work prosocially first, with others, then lock things down for yourself.
3. Proximity vs. Remoteness
   1. Like your body, keep your cloud personal
4. Sustainability[^2] over Tragedies of Commons to **not**
   - Systematically increase concentrations of substances extracted from the Earth's crust
   - Systematically increase concentrations of substances produced by society
   - Systematically increase degradation by physical means
   - Systematically undermine people's capacity to meet their needs

For example:

- Would everyone in the world having a personal cloud be deemed sustainable?
  - If not, then we need to go back to the drawing board, and learn to invent and apply technology in a sustainable way.

## How to Think

Examples of though process to improve our collective decision making.

## Be Tactical

While the above are abstract, we need to make things happen.

When in doubt:

- write code over thinking
- reflect over repeating
- go outside for a walk, give your ass a break[^3], meet people, and eat healthy sustainably produced food[^4]

[^1] [Optimizing the UX honeycomb](https://uxdesign.cc/optimizing-the-ux-honeycomb-1d10cfb38097)
[^2] [4 Principles to Win the Sustainability 'Game' (conditions of success)](https://www.youtube.com/watch?v=BO9_hQO9nTo)
[^3] remind yourself to take breaks with [Workrave](https://workrave.org/)
[^4] shop from organizations like [Lufa Farms](https://lufa.com/)

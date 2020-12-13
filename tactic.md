---
title: Tactic
description: Pragmatic Robust Action
img: first-blog-post.jpg
alt: my first blog post
author:
  name: Paul Cuciureanu
  bio: Hacker
  image: http://lorempixel.com/g/400/200/
---
# Tactic

Defend in large numbers:

- use cloud native technologies built by industry heavyweights to our personal collective privacy advantage. To do so, we must therefore:
  - stay up to date with industry trends
    - bleed at the bleeding edge, but only a little
- use off-the-shelf equipment
  - your last generation desktops, all together in a cluster, should allow to run most apps
- code directly in production
  - remember, this is your personal cloud, it's better to think that your network has already been owned, and still password protect your laptop, etc.
  - traditionally, staging environments are orders of magnitude smaller than production environments. Since the personal cloud is a cloud for one person or a few persons (a family, or at most a local community), running a full staging environment adds undue complexity
  - practice defensive programming and security
    - write tests
      - end to end
      - unit
    - use static typing
    - sandbox and containerize
    - backup everything often
      - to multiple physical locations
    - encrypt your data
    - hardware wallets
    - use multi-factor authentication
    - minimize the surface area of attack, i.e.: use less technology—ok, this one isn't too practical for our project

## Open Inquiry

1. How to handle secrets?
   - Do use:
     - Hardware wallets like the [Trezor Model T](https://trezor.io/)
     - Trustworthy OS like [Qubes OS](https://www.qubes-os.org/)
     - Open Hardware:
       - [Librem 5](https://puri.sm/products/) mobile phone
       - [System76](https://system76.com/) laptops and desktops
       - [Turris Omnia](https://www.turris.com/en/omnia/overview/) home router
       - [RISC-V](https://riscv.org/)
     - Open Software:
       - [Almond](https://almond.stanford.edu/) Virtual Assistant
       - Self-host all the critical stuff
         - Air-gap[^1] what you don't want leaked for improved security
   - Don't use:
     - …mostly everything you can purchase off the shelf—buyer beware!
     - Proprietary systems whose operations can't be audited by you in person
       - This includes all VPN and public cloud providers
   - With that said, we're willing to compromise **for now** (this is temporary!) and rely on others until we learn to secure our digital selves, one piece of data at a time
     - Ok to use a 3rd party IAM system like the [Pulumi Service backend](https://www.pulumi.com/docs/intro/concepts/state/#pulumi-service-backend)
     - Ok to use a 3rd party proprietary system like [1Password](https://1password.com/)
     - Ok to use a classic retail bank until you understand and are fluent with crypto payments

[^1] [What is an Air Gapped Computer?
](https://www.thesslstore.com/blog/air-gapped-computer/)

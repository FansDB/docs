---
title: Home
hide:
  - navigation
---

## What is FansDB?

FansDB is invite-only crowdsourced metadata database focused on independent adult content creators and adult platforms. It runs on stash-box[^1] which uses perceptual hashing[^2] to make matching your local files to FansDB metadata very easy. It elimates the common struggle of unreliable filenames or files being in different resolution not matching.

To take full advantage of it, you just need ot install Stash[^3] porn organizer application. It will be able to connect directly to the FansDB. Follow their documentation[^4] for installation instructions.

## Accessing FansDB

1. Submit an [application to join](https://cryptpad.fr/form/#/2/form/view/YfCcSl4CTKvvNyMyAS17YdEy2VRNOLP-zKLZ2kcUdrU/){target=_blank}.
2. Once you receive an invitation code, register an account at [https://fansdb.cc/register](https://fansdb.cc/register){target=_blank}.
3. Login using your username (not email) and password. 
4. While logged in, click on your username at the top of the menu bar and find an **API key** and **GraphQL Endpoint** sections. 
5. Go to your local Stash and go to `Settings` > `Metadata Providers` > `Stash-box Endpoints` > `Add`.
6. Enter the **Name**, **GraphQL endpoint**, **API key** and click `Confirm`. You can also click `Test Credentials` to make sure everything is correct.
7. The endpoint is now added and can be used to scrape metadata like with any other scraper. 

[^1]: [stash-box repository](https://github.com/stashapp/stash-box){target=_blank}
[^2]: Perceptual hashing allows you to compare similartities between multiple multimedia files by hamming distance. Which means that despite difference in resolution, encoding or basic changes to the source file it can still be grouped together and matched easily. Read more about it [here](https://en.wikipedia.org/wiki/Perceptual_hashing){target=_blank}.
[^3]: [Stash repository](https://github.com/stashapp/stash){target=_blank}
[^4]: [Stash installation](https://docs.stashapp.cc/installation){target=_blank}

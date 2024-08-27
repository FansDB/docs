---
title: Home
hide:
  - navigation
---

# Home

## What is FansDB?

FansDB is a user-curated metadata database focused on individual adult content creators. It runs on stash-box[^1] which takes advantage of perceptual hashing to make matching your existing files to metadata stored on FansDB super easy, barely an inconvenience. 

To make the most of it you should also install a local adult content organizer called Stash[^2] developed by the same team. Follow their documentation[^3] to get started.

## Accessing FansDB

1. Submit an [application to join](https://cryptpad.fr/form/#/2/form/view/YfCcSl4CTKvvNyMyAS17YdEy2VRNOLP-zKLZ2kcUdrU/){target=_blank}.
2. Once you receive an invitation code, register an account at [https://fansdb.cc/register](https://fansdb.cc/register){target=_blank}.
3. Login using your username (not email) and password. 
4. While logged in, click on your username at the top of the menu bar and find an **API key** and **GraphQL Endpoint** sections. 
5. Go to your local Stash and go to `Settings` > `Metadata Providers` > `Stash-box Endpoints` > `Add`.
6. Enter the **Name**, **GraphQL endpoint**, **API key** and click `Confirm`. You can also click `Test Credentials` to make sure everything is correct.
7. The endpoint is now added and can be used to scrape metadata like with any other scraper. 

[^1]: [stash-box repository](https://github.com/stashapp/stash-box){target=_blank}
[^2]: [Stash repository](https://github.com/stashapp/stash){target=_blank}
[^3]: [Stash documentation](https://docs.stashapp.cc/getting-started/){target=_blank}
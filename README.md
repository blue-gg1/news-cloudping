# cloudping.info Website Source

<https://cloudping.info/>

The website is hosted on [GitLab Pages](https://pages.gitlab.io/).

# How to Change the Website

1. Make a gitlab.com account
2. Fork this repository
3. Commit changes to your fork
4. Create a Pull Request (PR) to merge your changes into this repository.
5. Email a signed copy of [`cla-email-template.txt`](https://gitlab.com/leonhard-llc/cloudping.info/-/blob/master/cla-email-template.txt)
6. Respond to comments on your PR
7. When we merge your changes, they go live immediately.

# Contributors
- [Tayyab Mughal](https://gitlab.com/back2Lobby)
  updated the code to use `async` and the Fetch API

Thank you!

# TO DO
[X] Modernize code,
use [`await`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await) and
the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API).
[X] Continue after error
[ ] Timeout after 10s
[ ] Use CORS for services that support it (AWS)
[ ] Ping multiple endpoints at once
[ ] Add a visual indicator of relative latency,
    to help users find the fastest regions without reading the milliseconds numbers. 
[X] Add AWS
[X] Add DigitalOcean
[ ] Add Linode
[ ] Add Azure
[ ] Add Google Cloud
[ ] Add IBM Cloud
[ ] Add Hetzner
[ ] Add OVH
[ ] Add other cloud providers.

# Known Problems

1. DigitalOcean does not support CORS.
   When pinging a DigitalOcean endpoint,
   if the request fails quickly,
   the page shows an impossibly short time, like 4ms.
   Ideally, it would show "error".
   To accomplish that, we need an endpoint that supports CORS.
   Running my own would cost $5/mo per region, or $780/year.
   To cover this cost, I could sell ads or move the project to GitHub and accept donations.

# How to Report a Problem
1. Go to https://gitlab.com/leonhard-llc/cloudping.info/-/issues
2. Click "Register" and create a gitlab.com account
3. Go back to https://gitlab.com/leonhard-llc/cloudping.info/-/issues and click "New Issue"
4. Enter a clear description of the problem

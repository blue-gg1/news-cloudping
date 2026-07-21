# cloudping.info Website Source

<https://cloudping.giedi-prime.org/>

# Contributors
- [Michael Leonhard](https://gitlab.com/leonhard-llc) author
- [Justin Briard](https://gitlab.com/jbriard) added support for Vultr.
- [Anas Shakil](https://gitlab.com/anasshakil) added support for Google Cloud, Hetzner, and a new AWS region.
- [Tayyab Mughal](https://gitlab.com/back2Lobby)
  updated the code to use `async` and the Fetch API.

Thank you!

# TO DO
- [X] Modernize code,
  use [`await`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)
  and the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API).
- [X] Continue after error
- [X] Timeout after 5s
- [X] Use CORS for services that support it (AWS)
- [X] Ping multiple endpoints at once
- [x] Add a visual indicator of relative latency, 
  to help users find the fastest regions without reading the milliseconds numbers. 
- [X] Add AWS
- [X] Add DigitalOcean
- [X] Add Linode
- [X] Add IBM Cloud
- [X] Add OVH Cloud
- [X] Add Scaleway Cloud
- [X] Add Vultr - [Issue #3](Cloud https://gitlab.com/leonhard-llc/cloudping.info/-/issues/3)
- [ ] Add Azure - [Issue #6](https://gitlab.com/leonhard-llc/cloudping.info/-/issues/6)
- [X] Add Google Cloud - [Issue #7](https://gitlab.com/leonhard-llc/cloudping.info/-/issues/7)
- [x] Add Hetzner - [Issue #8](https://gitlab.com/leonhard-llc/cloudping.info/-/issues/8)
- [ ] Add other cloud providers.

# Known Problems

## Shows very small latency number instead of error
The URLs we're using for DigitalOcean & Linode do not support CORS.
This means that JavaScript provides the same generic "network error" value
for success and for all kinds of network errors.
We measure the time it takes to return the error.
Unfortunately, some errors come back immediately and then the page shows an incorrect short time, like 4ms.

We would like it to show "error" instead.
To get that, we need servers that support CORS in each region.
Running my own would cost $5/month per region x 13 DigitalOcean regions and 11 Linode regions,
or $1440/year.
To cover this cost, the site could sell ads,
move the project to GitHub and accept donations,
or use affiliate links.
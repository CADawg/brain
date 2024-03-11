---
dg-publish: true
---

I saw [this post](https://medium.com/hoppinger/profiling-the-hidden-costs-of-json-and-http-s-c8f327d5db89) today about using HTTPS requests + JSON vs Websockets + Binary or Websockets + JSON. I've played around with websockets a little bit before, but seems like it could be useful for high throughput apps (or apps that send a lot of data to the browser). The request time savings are immense almost to the point of being as good as that of enabling a CDN on a website, so I'd like to give this a shot in a project where it makes sense.
---
layout: post
title: What is RawGit and how can it help you to host your site through gitHub pages
---
When you request a file from source control hosting services, they are usually served (in the case of JavaScript, HTML, CSS, and some other file types) with a Content-Type of text/plain. As a result, most modern browsers won't actually interpret it as JavaScript, HTML, or CSS.

They do this because serving raw files from a git repo is relatively inefficient, so they want to discourage people from using their repos for static file hosting.

raw.githack.com acts as a caching proxy, forwarding requests to the corresponding service, caching the responses either for a short time (in the case of development URLs) or permanently (in the case of CDN URLs), and relaying them to your browser with the correct Content-Type headers.

The caching layer ensures that minimal load is placed on each service, and you get quick and easy static file hosting right from a repo. Everyone's happy!

<h3>What's the difference between development and CDN URLs?
</h3>
When you make a request to a development URL, the server loads the requested file from the corresponding service, serves it to your browser with the correct Content-Type header, and caches it for a short time. If you push new changes to your repo, you can reload and see them within a few minutes, which makes development URLs useful for low-traffic testing or sharing demos during development.

Requests to CDN are routed through CloudFlare's content delivery network, and are cached for a year the first time they're loaded. This results in the best performance and reduces load on raw.githack.com and on underlying service, but it means that reloading won't fetch new changes. Furthermore, JS and CSS files will be minified for the sake of performance.

During development, when traffic is low and freshness is more important than performance, use development URLs. For anything you share with the public or push to production, use CDN URLs
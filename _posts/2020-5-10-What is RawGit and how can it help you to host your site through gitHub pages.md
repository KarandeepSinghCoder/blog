---
layout: post
title: What is RawGit and how can it help you to host your site through gitHub pages.
---
When you request a file from source control hosting services, they are usually served (in the case of JavaScript, HTML, CSS, and some other file types) with a Content-Type of text/plain. As a result, most modern browsers won't actually interpret it as JavaScript, HTML, or CSS.

They do this because serving raw files from a git repo is relatively inefficient, so they want to discourage people from using their repos for static file hosting.

raw.githack.com acts as a caching proxy, forwarding requests to the corresponding service, caching the responses either for a short time (in the case of development URLs) or permanently (in the case of CDN URLs), and relaying them to your browser with the correct Content-Type headers.

The caching layer ensures that minimal load is placed on each service, and you get quick and easy static file hosting right from a repo. Everyone's happy!
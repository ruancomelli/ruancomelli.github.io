+++
title = "Building a blog with Zola and GitHub Pages"
date = 2025-10-27
updated = 2025-10-27
description = "How I built this blog using Zola, a static site generator, and deploying it to GitHub Pages."

[taxonomies]
tags = ["tutorial"]

[extra]
quick_navigation_buttons = true
toc = true
# social_media_card = "social_cards/blog_comments.jpg"
+++

## Preface

In early 2025, I left my job at [Sourcery AI](https://sourcery.ai/), marking the first time I had nothing to do<sup>(besides looking for a new job)</sup> after a 6-year streak of a Master's in Mechanical Engineering followed by two jobs as a software engineer. This looked like the perfect opportunity to try out new things, like studying Rust. Or writing a blog.

I've already talked about my goals and expectations regarding this site in [the Hello World post](../hello-world/). In this post, I'd like to walk you through how I built this site and explain the decisions I made along the way.

## Picking a static site generator

### Why Zola?

<!-- TODO: or mention "Zola" directly? -->

<!-- TODO: introduce this -->

Static site generators (SSGs) are tools that use templates to convert content files into HTML (plus CSS and JS) pages. <!-- TODO:  -->

When searching for a SSG to use, I set the following constraints:

- **Multi-language support**: I want to be able to write posts both in English and Portuguese for two reasons. The first one is to be able to practice my writing skills in both languages. The second one is to be able to reach a wider audience with English content while also giving a special attention to Brazilians;
- **Simple and lightweight**: I want to focus on writing content, not on managing a complex build system;
- **Customizable**: I also want to be able to customize the look and feel of the site to my liking, if needed;
- **Open source**: I want to be able to contribute to the project if I need to, and I want to be able to use the code for my own projects.
- **Performance**: I want the site to be fast and efficient, and I want to be able to easily add new features and improve the site over time.

On the other hand, some non-constraints&mdash;that is, things I was willing to compromise on&mdash;were:

- **Good community support and documentation**: community support and documentation are important, but I am willing to try out new tools. The good thing with writing this site is that there's no external pressure
- **SEO**: I am really not worried about SEO for this site. Luckily, the Zola SSG and the Tabi theme I ended up using are both SEO-friendly; but it wouldn't be a dealbreaker if they weren't.

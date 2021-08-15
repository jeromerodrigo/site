---
title: "Hello World"
date: 2021-08-14T18:00:00+08:00
tags: ["hugo", "web", "personal"]
draft: false
summary: "New personal site & fun with hugo static site generator."
---

# 👋 Hello (again)

It's been a while since I've written a blog. And when I say "a while"
it's actually been more than a decade. However, blogging was where I started
my passion to tweak and tinker with websites. 

It all started when [Blogger](https://en.wikipedia.org/wiki/Blogger_%28service%29) became a big hit circa 2003. I was in my first year of high school. One thing lead to another, and BOOM I'm now a fully fledged software engineer. This probably deserves another post, but I digress.

## Why hugo

Ever since hearing about static site generators (SSGs) like [Jekyll](https://jekyllrb.com/) gain popularity, I was curious about how it all worked. Plus we can get free hosting on GitHub pages! However, I pretty much know nothing about Ruby (personally don't have much interest to learn it right now).

I was also playing around with [Golang](https://golang.org/) at the time, when I heard about [Hugo](https://gohugo.io/). I can't really compare the two because I have not tried Jekyll, however my experience setting up Hugo was really easy.

As easy as `hugo new site <sitename>`.

## A few things that helped

This post isn't intended to be a step-by-step tutorial, rather it's a journal of what my experience was building this personal site for myself.

### 📖 Tutorials help!

Not knowing much about using Hugo, this [Make a Hugo Blog From Scratch](https://zwbetz.com/make-a-hugo-blog-from-scratch/) tutorial really got me started.


### [Bootstrap CSS](https://getbootstrap.com/) for the UI
Bootstrap is a framework that I'm familiar with and it works well for my simple use case, which is this personal site and blog.


### 🏀 Design inspiration from [dribbble](https://dribbble.com/search/portfolio)

The designs people upload here are just amazing. This really helped inspire how I wanted my portfolio page to look.

Good for me since I'm not a professional designer. Best to learn from others!

## 🔨 Challenges & 💡 Learnings

### #1 Making designs

I think I spent a lot longer than I intended in designing the projects and skills section. However once I got started, everything fell into place 🙂

### #2 Implementing **responsive layout** involved a lot of trial and error

After many tries I managed to get it just nice, thanks to the [docs](https://getbootstrap.com/docs/5.1/layout/grid/).

### #3 String concatenation

This shouldn't be an issue in plain Golang. However in the context of Hugo
I couldn't really figure out what was the best way to concatenate two strings.

This is what I ended up with
```
{{ $video := index .vid }}
{{ if ne $video "" }}
{{ $url := print "video/" $video }}
```

Feels a bit strange to use a `print` function to combine `video/` and the `#video` variable that holds the actual video file name.

### #4 Avoiding repetition in `hugo`

Hugo has great templating features that I wished I knew earlier. I had already spent a considerable amount of time hand-coding a lot of the HTML.

After learning to do this
```html
{{ range .Site.Data.home.projects }}
<div>{{ index .name }}</div>
{{ end }}
```
Life became much easier.

Hugo has a `/data` folder where you can define custom front matter. This way I can maintain content in one place, and keep the HTML/CSS solely for the presentation aspect of that content.

## Conclusion

It's great to finally have my own site, wished I had done this earlier. Currently have no real plans on a consistent blogging schedule, but the idea of producing more content definitely interests me.

Let's see how it goes. 🤠
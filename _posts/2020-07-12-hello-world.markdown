---
layout: post
title:  "Hello world!"
date:   2020-07-12 0:00:08 +0300
categories: jekyll update
---

Nice to see how markdown file becomes a post.

## How I met my blog

Though it was a bit tough to create proper ruby environment on WSL Ubuntu 18.04, I managed Jekyll to create my blog.

Here are two docs which I use for blog construction:
- Installation - https://jekyllrb.com/docs/installation/
- Blog creation - https://jekyllrb.com/docs/

I run into problems since beginning when trying to create proper ruby environment. `rbenv` declined to install 2.5.0 `ruby` with
```
BUILD FAILED (Ubuntu 18.04 using ruby-build 20170726)
```

Found these instructions but following them didn't worked for me:
- https://github.com/rbenv/ruby-build/issues/1199
- https://github.com/rvm/rvm/issues/4764#issuecomment-545827887

After that I decided to do a straight `apt-get install ruby`. This brings to me `2.5.1` version which is nice.

Next I got build error when trying to `gem install jekyll bundler`. Apparentely, I missed `ruby-dev` package when installing `ruby` since `jekyll` couldn't build in the first time complaining about some `ruby` headers.

Also I `chown`-ed `/var/lib/gems/` to my local user so I can use gems without `sudo` ... as I thought. I discover that `ruby` still want root when building some necessary gems (to access those headers or something like that, I guess).

Finally after all commands succeeded, running
```bash
jekyll new myblog
cd myblog
bundle exec jekyll serve
```
brings calm to my heart.

## In conclusion

Setting up environement is the hardest 80% in almost every project. Doing the project is the rest 80%, while supporting it through years takes another 146%.

Wish luck to myself and you.

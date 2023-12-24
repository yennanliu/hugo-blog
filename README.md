# hugo-blog

## Setup

```bash
brew install hugo
```

## Run

```bash

# (base) yennanliu@MacBook-Pro hugo-blog % ls
# README.md hugodemo
# (base) yennanliu@MacBook-Pro hugo-blog % cd hugodemo
# git init
# git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
# Initialized empty Git repository in /Users/yennanliu/hugo-blog/hugodemo/.git/
# Cloning into '/Users/yennanliu/hugo-blog/hugodemo/themes/ananke'...
# remote: Enumerating objects: 2694, done.
# remote: Counting objects: 100% (123/123), done.
# remote: Compressing objects: 100% (75/75), done.
# remote: Total 2694 (delta 61), reused 88 (delta 41), pack-reused 2571
# Receiving objects: 100% (2694/2694), 4.52 MiB | 7.75 MiB/s, done.
# Resolving deltas: 100% (1494/1494), done.
# (base) yennanliu@MacBook-Pro hugodemo % echo theme = "ananke" >> config.toml
# (base) yennanliu@MacBook-Pro hugodemo % hugo new posts/my-first-post.md
# Content "/Users/yennanliu/hugo-blog/hugodemo/content/posts/my-first-post.md" created
# (base) yennanliu@MacBook-Pro hugodemo % hugo server
# Watching for changes in /Users/yennanliu/hugo-blog/hugodemo/{archetypes,assets,content,data,i18n,layouts,static}
# Watching for config changes in /Users/yennanliu/hugo-blog/hugodemo/hugo.toml
# Start building sites …
# hugo v0.121.1-00b46fed8e47f7bb0a85d7cfc2d9f1356379b740+extended darwin/amd64 BuildDate=2023-12-08T08:47:45Z VendorInfo=brew

# WARN  found no layout file for "html" for kind "taxonomy": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
# WARN  found no layout file for "html" for kind "home": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.

#                    | EN
# -------------------+-----
#   Pages            |  3
#   Paginator pages  |  0
#   Non-page files   |  0
#   Static files     |  0
#   Processed images |  0
#   Aliases          |  0
#   Sitemaps         |  1
#   Cleaned          |  0

# Built in 11 ms
# Environment: "development"
# Serving pages from memory
# Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
# Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
# Press Ctrl+C to stop


# run app
hugo server

# http://localhost:1313
```

## Development

## Ref
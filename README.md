# hugo-blog

## Setup

```bash
brew install hugo
```

## Run

```bash

# hugo new site quickstart
# cd quickstart
# git init
# git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
# echo "theme = 'ananke'" >> hugo.toml
# hugo server


# create post
cd quickstart

hugo new content posts/my-first-post.md
hugo new content posts/my-second-post.md

# rebuild
hugo

# run app
cd quickstart

# run app show publish posts
hugo server

# run app show drafts
hugo server --buildDrafts
# or
hugo server -D

# http://localhost:1313
# http://localhost:1313/posts/my-first-post/
```

## Development

- Update config
 - `hugo.toml` at root path
- Static path
 - `quickstart/themes/ananke/static/ads.txt`
 	- http://localhost:1313/ads.txt


## Deployment

- Netlify
	- https://app.netlify.com/sites/frabjous-buttercream-835594/overview

## Ref

- Hugo
	- https://gohugo.io/getting-started/quick-start/

- Google adsense
	- https://adsense.google.com/start/
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

## Ref

- https://gohugo.io/getting-started/quick-start/
# Development

``` bash
npx tailwindcss-cli@latest build ./src/tailwind.css -o ./assets/css/tailwind.css
bundle exec jekyll serve --livereload
```

# Deployment

When building for production, always set JEKYLL_ENV=production and NODE_ENV=production on the command line. When these variables are set to production, unused Tailwind styles are purged and the output is processed with cssnano.

``` bash
NODE_ENV=production npx tailwindcss-cli@latest build ./src/tailwind.css -o ./assets/css/tailwind.css
JEKYLL_ENV=production NODE_ENV=production bundle exec jekyll build
```
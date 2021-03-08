# References

- [Step by Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/)
- [Jekyll Cheat Sheet](https://learn.cloudcannon.com/jekyll-cheat-sheet/)
- [Liquid](https://shopify.github.io/liquid/)
- [Liquid template language reference](https://shopify.dev/docs/themes/liquid/reference)
- [About GitHub Pages and Jekyll](https://docs.github.com/en/github/working-with-github-pages/about-github-pages-and-jekyll)
- [Setting up a GitHub Pages site with Jekyll](https://docs.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)
- [Tailwind CSS docs](https://tailwindcss.com/docs)


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


# Rails 7 new and setup

In your terminal run \
`rails new my_quotes_app --database=postgresql --css=sass --javascript=esbuild --skip-active-storage`

## Subtle setup!

You might not have seen it but in your logs it asked you to add below scripts to your `package.json` \
```javascript
  "scripts": {
    "build": "esbuild app/javascript/*.* --bundle --sourcemap --outdir=app/assets/builds",
    "build:css": "sass ./app/assets/stylesheets/application.sass.scss ./app/assets/builds/application.css --no-source-map --load-path=node_modules"
  }
```
<img width="1156" alt="Screenshot 2565-04-07 at 21 45 27" src="https://user-images.githubusercontent.com/33062224/165052725-79f5f170-d262-41a9-9eff-f7a049600d56.png">
<img width="1280" alt="Screenshot 2565-04-07 at 21 45 48" src="https://user-images.githubusercontent.com/33062224/165052732-865a000c-4b23-48cd-87d3-62722bc385b0.png">


## Finalize the setup
In your terminal run \
`bin/setup` \
`bin/dev` \
A `yarn build:css` might also be necessary

## Useful links
[Managing JS and CSS Assets in Rails 7](https://www.csalmeida.com/log/managing-js-and-css-assets-in-rails-7/)

## JS for animation
https://michalsnik.github.io/aos/
```html
   <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
      AOS.init({once: true,});
    </script>
```

# Sinatra Boilerplate

This boilerplate extends Sinatra with the following features:

  * [Haml](http://haml-lang.com/) + HTML5
  * [Sass](http://sass-lang.com/) + [Compass](http://compass-style.org/)
  * [CoffeeScript](http://coffeescript.org/) + concatenation & compression
  * [LiveReload guard](https://github.com/guard/guard-livereload) +
    [Foreman](https://github.com/ddollar/foreman)

## JavaScript Assets

To enable concatenation and compression, you need to define your JavaScripts assets:

```ruby
set :js_assets, %w[zepto.js underscore.js app.coffee]
```

Regular `.js` files must be under `public/`, and `.coffee` files under `views/`.

Now use the `javascripts_includes` helper to render `<script>` tags. No
need to define their routes!

In production mode all JavaScript assets will be served from `/all.js`
which is a special resource that concatenates and compresses all files.

## LiveReload guard

In order for LiveReload guard to work, you need to install the [browser
extension](https://github.com/guard/guard-livereload), if you haven't
already.

Each time you save your `.haml`, `.s[ac]ss` or `.coffee` files in your
`views/`, your browser will automatically refresh! To customize
LiveReload guard, you can edit the `Guardfile`. Learn more about Guard
and `Guardfile`s in [Guard's
documentation](https://github.com/guard/guard#readme).

## Starting Your App

To start your app, run:

    $ foreman start

Now go to `localhost:4567` and enable LiveReload. Each time you edit 

## Troubleshooting

If you don't have the `foreman` command, it might be because you didn't
run `bundle exec`. Or you did, but you have some kind of a Ruby version
management system. Try running `gem pristine foreman` and re-generating
your shims.

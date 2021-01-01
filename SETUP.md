# Setup Phoenix project

## setup

```bash
$ mix phx.new . --app sample_app --no-ecto

* creating config/config.exs
* creating config/dev.exs
* creating config/prod.exs
* creating config/prod.secret.exs
* creating config/test.exs
* creating lib/sample_app/application.ex
* creating lib/sample_app.ex
* creating lib/sample_app_web/channels/user_socket.ex
* creating lib/sample_app_web/views/error_helpers.ex
* creating lib/sample_app_web/views/error_view.ex
* creating lib/sample_app_web/endpoint.ex
* creating lib/sample_app_web/router.ex
* creating lib/sample_app_web/telemetry.ex
* creating lib/sample_app_web.ex
* creating mix.exs
* creating README.md
* creating .formatter.exs
* creating .gitignore
* creating test/support/channel_case.ex
* creating test/support/conn_case.ex
* creating test/test_helper.exs
* creating test/sample_app_web/views/error_view_test.exs
* creating lib/sample_app_web/controllers/page_controller.ex
* creating lib/sample_app_web/templates/layout/app.html.eex
* creating lib/sample_app_web/templates/page/index.html.eex
* creating lib/sample_app_web/views/layout_view.ex
* creating lib/sample_app_web/views/page_view.ex
* creating test/sample_app_web/controllers/page_controller_test.exs
* creating test/sample_app_web/views/layout_view_test.exs
* creating test/sample_app_web/views/page_view_test.exs
* creating lib/sample_app_web/gettext.ex
* creating priv/gettext/en/LC_MESSAGES/errors.po
* creating priv/gettext/errors.pot
* creating assets/webpack.config.js
* creating assets/.babelrc
* creating assets/js/app.js
* creating assets/css/app.scss
* creating assets/js/socket.js
* creating assets/package.json
* creating assets/static/favicon.ico
* creating assets/css/phoenix.css
* creating assets/static/images/phoenix.png
* creating assets/static/robots.txt

Fetch and install dependencies? [Yn] 
* running mix deps.get
* running mix deps.compile
* running cd assets && npm install && node node_modules/webpack/bin/webpack.js --mode development

We are almost there! The following steps are missing:

    $ cd phoenix_local_playground_no_ecto

Start your Phoenix app with:

    $ mix phx.server

You can also run your app inside IEx (Interactive Elixir) as:

    $ iex -S mix phx.server

```

```bash
$ mix deps.get && mix deps.compile
```

```bash
$ cd assets && npm install && node node_modules/webpack/bin/webpack.js --mode development
```

## run

```bash
$ mix phx.server
Compiling 13 files (.ex)
Generated sample_app app
[info] Running SampleAppWeb.Endpoint with cowboy 2.8.0 at 0.0.0.0:4000 (http)
[info] Access SampleAppWeb.Endpoint at http://localhost:4000

webpack is watching the files…

[hardsource:6ce59752] Using 1 MB of disk space.
[hardsource:6ce59752] Writing new cache 6ce59752...
[hardsource:6ce59752] Tracking node dependencies with: package-lock.json.
Hash: 1da64221c352f7411d41
Version: webpack 4.41.5
Time: 1173ms
Built at: 2020-12-15 9:19:49
                Asset       Size  Chunks             Chunk Names
       ../css/app.css   10.7 KiB     app  [emitted]  app
       ../favicon.ico   1.23 KiB          [emitted]  
../images/phoenix.png   13.6 KiB          [emitted]  
        ../robots.txt  202 bytes          [emitted]  
               app.js   13.5 KiB     app  [emitted]  app
Entrypoint app = ../css/app.css app.js
[0] multi ./js/app.js 28 bytes {app} [built]
[../deps/phoenix_html/priv/static/phoenix_html.js] 2.21 KiB {app} [built]
[./css/app.scss] 39 bytes {app} [built]
[./js/app.js] 490 bytes {app} [built]
    + 2 hidden modules
Child mini-css-extract-plugin node_modules/css-loader/dist/cjs.js!node_modules/sass-loader/dist/cjs.js!css/app.scss:
    Entrypoint mini-css-extract-plugin = *
    [./node_modules/css-loader/dist/cjs.js!./css/phoenix.css] 10.4 KiB {mini-css-extract-plugin} [built]
    [./node_modules/css-loader/dist/cjs.js!./node_modules/sass-loader/dist/cjs.js!./css/app.scss] 1 KiB {mini-css-extract-plugin} [built]
        + 1 hidden module
[info] GET /
[debug] Processing with SampleAppWeb.PageController.index/2
  Parameters: %{}
  Pipelines: [:browser]
[info] Sent 200 in 20ms

```

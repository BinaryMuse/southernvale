# The Southern Vale

Source code for https://southernvale.net

## Installing

Requires [Bundler](http://bundler.io/).

```bash
bundle --path vendor
```

If you're on macOS and have trouble with Nokogiri, try:

```bash
bundle config build.nokogiri --use-system-libraries=true --with-xml2-include="$(xcrun --show-sdk-path)"/usr/include/libxml2
bundle --path vendor
```

## Previewing Site Locally

```bash
bundle exec rake preview
```

The site will be available at http://localhost:4000.

## Building Site

```bash
bundle exec rake build
```

The site will be built into `_site/`.

## Publishing Site

Requires that [now CLI](https://zeit.co/download#now-cli) is installed.

```bash
bundle exec rake sync
```

Note that you can build and publish the site at the same time with `bundle exec rake publish`.

# emmasax4-redirects

This repository is designed to be temporary to assist in creating solid 301 redirects from the following domains to `https://emmasax4.com`.

* `http://emmasax4.info`
* `https://emmasax4.info`
* `http://www.emmasax4.info`
* `https://www.emmasax4.info`

What I've done is taken every single `index.html` file that could be served at `emmasax4.info` (viewable by looking at the files [here](https://github.com/emmasax4/emmasax4.com/tree/dd3f3500597331bf4795746d4d1ecdb60b0bb21c) and recreated the directory structure and `index.html` files in this repository. The content of each `index.html` file looks like this:

```html
<!DOCTYPE html>
<html lang="en-US">
  <meta charset="utf-8">
  <title>Redirecting&hellip;</title>
  <link rel="canonical" href="https://emmasax4.com/path/and/file/name/">
  <script>
    location="https://emmasax4.com/path/and/file/name/"
  </script>
  <meta http-equiv="refresh" content="0; url=https://emmasax4.com/path/and/file/name/">
  <meta name="robots" content="noindex">
  <h1>Redirecting&hellip;</h1>
  <a href="https://emmasax4.com/path/and/file/name/">Click here if you are not redirected.</a>
</html>
```

I didn't bother filling it with a bunch of other unnecessary files, which is why the majority of this repository is so empty.

My plan from here on out is to keep this repository and the old domain (`emmasax4.info`) alive for about six months while my SEO ratings come back. And then, I can sunset this repository and just put in plain `http` redirects in my domain name registrar going forward.

Huge thanks to Oleksii Tsvietnov for [the idea](https://opensource.com/article/19/7/permanently-redirect-github-pages).

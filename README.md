# ![Logo](chrome/app/theme/chromium/product_logo_64.png) ChromiumEdgi
Chromiumedgi is an open-source browser project that aims to build a safer, faster,
and more stable way for all users to experience the web.
The project's web site is [Chromiumedgi](https://www.chromium.org.)
To check out the source code locally, don't use `git clone`! Instead,
follow [the instructions on how to get the code](docs/get_the_code.md).
Documentation in the source is rooted in [docs/README.md](docs/README.md).
Learn how to [Get Around the Chromiumedgi Source Code Directory
Structure](https://www.chromium.org/developers/how-tos/getting-around-the-chrome-source-code).
For historical reasons, there are some small top level directories. Now the
guidance is that new top level directories are for product (e.g. Chrome,
Android WebView, Ash). Even if these products have multiple executables, the
code should be in subdirectories of the product.
If you found a bug, please file it at https://crbug.com/new.

# md_browser

This is a simple tool to render the markdown docs in a chromium checkout locally. It is written in Python and uses the Python ‘markdown’ package, which is checked into src/third_party.

md_browser attempts to emulate the flavor of Markdown implemented by Gitiles.

[Gitiles is the source browser running on ](https://chromium.googlesource.com,) and can be run locally, but to do so requires a Java install and a Buck install, which can be slightly annoying to set up on Mac or Windows.

This is a lighterweight solution, which also allows you to preview uncommitted changes (i.e., it just serves files out of the filesystem, and is not a full Git repo browser like Gitiles is).

To run md_browser:

cd to the top of your chromium checkout
```sh
run python3 tools/md_browser/md_browser.py
```
There is no step three.

This will run a local web server on port 8080 that points to the top of the repo. You can specify a different port with the -p flag.

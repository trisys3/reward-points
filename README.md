# Reward Points

## Sample application for calculating reward points using a given data set

This application is available directly from the command line, which means no fiddling around with servers!

If you know where you cloned the repo, just put that path into your browser. For example, say you are using Cygwin or MSYS/MinGW and ran `git clone git@github.com:trisys3/reward-points.git /c/Users/me/reward-points`. In this case, the URL would be `file:///C:/Users/me/reward-points/index.html`.

This page works on all modern browsers. It WILL NOT work on Internet Explorer.

If you want to edit the code yourself, you need to install `npm`. I like to use `asdf` for this:

```
git clone git@github.com:asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"
. $HOME/.asdf/asdf.sh
asdf plugin add nodejs
asdf install nodejs latest
asdf local nodejs <version from previous command>
```

Then install the `npm` packages, e.g. `npm ci`. Finally, start webpack with `./webpack.config.mjs -- -w` to see your changes. Hot reloading is not set up, so you need to reload the browser to see changes.

If you made a simple change and want to see how it affected the page without starting a watch, run `./webpack.config.mjs` instead.

## Scenario

A retailer offers a rewards program to its customers, awarding points based on each recorded purchase.

A customer receives 2 points for every dollar spent over $100 in each transaction, plus 1 point for every dollar spent
over $50 in each transaction
(e.g. a $120 purchase = 2x$20 + 1x$50 = 90 points).

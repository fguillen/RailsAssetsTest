# Rails Assets Test

Mini application to reproduce the [StackOverflow issue](http://stackoverflow.com/questions/12235859/rails-3-assets-css-relative-urls)

## Install

    git clone git@github.com:fguillen/RailsAssetsTest.git
    cd RailsAssetsTest/
    bundle install

## Reproduce the issue

    rails s
    open http://localhost:3000

And you can see the icons like in [here](https://raw.github.com/fguillen/RailsAssetsTest/master/etc/development_icons.png)

    rake assets:precompile
    rails s -e production
    open http://localhost:3000

No icons and `404` error like in [here](https://raw.github.com/fguillen/RailsAssetsTest/master/etc/production_icons.png)

## How to solve it

Check the answer:

* http://stackoverflow.com/a/12239146/316700

And in the `testing` branch of this repository you'll find the commit that solves the issue:

* https://github.com/fguillen/RailsAssetsTest/commit/7330bf9a6ab71d6c7c39f40fecd39fbd5c204f6c


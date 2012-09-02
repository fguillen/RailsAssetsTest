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


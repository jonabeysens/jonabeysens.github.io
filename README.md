Welcome to my personal website!

# Instructions for installation (tested on Mac OS)
1. I had to to do following commands to make bundle work with commonmarker (from [here](https://stackoverflow.com/questions/63729369/commonmarker-gem-cannot-be-installed-needed-for-jekyll-macos)):
```
cd /Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/include/ruby-2.6.0

sudo ln -sf universal-darwin19 universal-darwin20
```

# Instructions to run it locally (tested on Mac OS)
1. Clone the repository and made updates as detailed above
1. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
1. Run `bundle clean` to clean up the directory (no need to run `--force`)
1. Run `bundle install --vendor/bundle` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Add the folder `vendor/` to .gitignore
1. Run `bundle exec jekyll liveserve` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.
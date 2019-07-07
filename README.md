## How to run it

Install [Ruby](https://rubyinstaller.org/downloads/)
> Use ruby (< 2.5) on Windows!

Install `bundler` and `jekyll`:

``` sh
gem install jekyll bundler
```

Install dependencies:

``` sh
bundle install
```

Run the server:

``` sh
bundle exec jekyll serve

# or simply

jekyll serve
```

## Deploy on GitHub

- [Use custom domain](https://help.github.com/en/articles/quick-start-setting-up-a-custom-domain)

## Issues

### GemNotFoundException

#### Error Msg

``` powershell
PS G:\MyProject\Web\ElixirEnglish\elixirenglish> bundle exec jekyll serve
Traceback (most recent call last):
        2: from e:/Ruby25-x64/bin/bundle:23:in `<main>'
        1: from E:/Ruby25-x64/lib/ruby/2.5.0/rubygems.rb:308:in `activate_bin_path'
E:/Ruby25-x64/lib/ruby/2.5.0/rubygems.rb:289:in `find_spec_for_exe': can't find gem bundler (>= 0.a) with executable bundle (Gem::GemNotFoundException)
```

#### Solution

https://www.ruby-forum.com/t/install-gems-problem-in-windows/182514/6

``` sh
gem update
gem update --system
ruby -v
```

### ruby (< 2.5)

``` powershell
PS G:\MyProject\Web\ElixirEnglish\elixirenglish> bundle exec jekyll serve
Could not find gem 'wdm (~> 0.1.0) x64-mingw32' in any of the gem sources listed in your Gemfile.
Run `bundle install` to install missing gems.
PS G:\MyProject\Web\ElixirEnglish\elixirenglish> bundle install
Fetching gem metadata from https://rubygems.org/...........
Fetching gem metadata from https://rubygems.org/.
Resolving dependencies...
Bundler could not find compatible versions for gem "ruby ":
  In Gemfile:
    ruby

    github-pages was resolved to 175, which depends on
      jemoji (= 0.8.1) was resolved to 0.8.1, which depends on
        html-pipeline (~> 2.2) was resolved to 2.7.1, which depends on
          nokogiri (>= 1.4) was resolved to 1.8.1, which depends on
            ruby  (< 2.5) x64-mingw32

Could not find gem 'ruby  (< 2.5)', which is required by gem 'nokogiri (>=
1.4)', in any of the relevant sources:
  the local ruby installation
```

#### Solution

Install ruby 2.4

source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
gem "jekyll", "~> 3.8.6"


# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "jekyll-theme-pirati", "~>8.4.3"

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-assets", "3.0.11"
  gem 'jekyll-environment-variables'
end


# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

gem "json" # For gem building
gem 'sprockets', '4.0.0.beta8'
gem 'uglifier', '~> 4.0.0'
gem "mini_magick"
# gem "autoprefixer-rails"
gem "image_optim"
gem "image_optim_bin" # Optional
gem "image_optim_pack"
# Make sure watch mode works A-OK on Windows too
gem "wdm", "~> 0.1.1" if Gem.win_platform?

# Uncomment this line for local development.
# gem "jekyll-theme-pirati", github: "pirati-web/jekyll-theme-pirati", branch: "master"

group :development, :test do
  gem "html-proofer"
end

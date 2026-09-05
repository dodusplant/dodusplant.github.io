source "https://rubygems.org"

# Use the github-pages gem instead of pinning Jekyll/kramdown/plugin versions
# yourself. This locks your local dev environment to the exact gem versions
# GitHub's own Pages build servers use right now - so security patches,
# Jekyll updates, and plugin compatibility are handled centrally by GitHub
# rather than something you track and update by hand.
#
# The lines below fetch the currently-deployed version number directly from
# GitHub at install time, so this Gemfile never goes stale on its own -
# every `bundle install` checks https://pages.github.com/versions.json for
# the version GitHub is running today.
require "json"
require "open-uri"
versions = JSON.parse(URI.open("https://pages.github.com/versions.json").read)
gem "github-pages", versions["github-pages"], group: :jekyll_plugins

# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "minima", "~> 2.0"

# jekyll-feed is already bundled with github-pages above, so it's not listed
# separately here - adding your own version pin for it could conflict with
# the exact version github-pages requires.

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", "~> 2.0"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.2.0", :install_if => Gem.win_platform?

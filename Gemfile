source "https://rubygems.org"

OVERRIDES = %w(jemoji jekyll-commonmark-ghpages)

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem "jekyll", git: "https://github.com/jekyll/jekyll", branch: "master"
versions.each do |gem_name, version|
  gem gem_name, version if gem_name.start_with?("jekyll-") && !OVERRIDES.include?(gem_name)
end

gem "jekyll-commonmark-ghpages",
  git: "https://github.com/github/jekyll-commonmark-ghpages",
  branch: "rouge-2-or-3"

gem "redcarpet" # 18F/federalist-docs
gem "uswds-jekyll" # 18F/federalist-docs
gem "jekyll_pages_api_search", group: :jekyll_plugins # 18F/federalist-docs

source "https://rubygems.org"

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem "jekyll", git: "https://github.com/jekyll/jekyll", branch: "master"
versions.each do |gem_name, version|
  gem gem_name, version, group: :jekyll_plugins if gem_name.start_with?("jekyll-") || gem_name == "jemoji"
end

gem "redcarpet" # 18F/federalist-docs
gem "uswds-jekyll" # 18F/federalist-docs

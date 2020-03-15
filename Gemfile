source "https://rubygems.org"

OVERRIDES = %w(
  jekyll-sass-converter
  jekyll-default-layout
  jekyll-remote-theme
)

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem "jekyll", git: "https://github.com/jekyll/jekyll", branch: "master"
versions.each do |gem_name, version|
  next if gem_name.start_with?("jekyll-theme-")
  gem gem_name, version if gem_name.start_with?("jekyll-") && !OVERRIDES.include?(gem_name)
end

gem "jemoji", versions["jemoji"]
gem "jekyll-include-cache"
gem "jekyll-remote-theme", ">= 0.4.2"

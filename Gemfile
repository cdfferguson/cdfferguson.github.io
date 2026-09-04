source "https://rubygems.org"

# Mirrors the exact gem set GitHub Pages builds with, so a local preview
# matches what gets published.
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows / JRuby timezone data and a file-watch helper for `jekyll serve`.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
gem "wdm", "~> 0.1", platforms: [:mingw, :x64_mingw, :mswin]

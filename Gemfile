source "https://rubygems.org"

# Same gem versions GitHub Pages uses, for local previews only.
# GitHub Pages builds the site itself; this file isn't needed for deploys.
gem "github-pages", group: :jekyll_plugins
gem "webrick" # Ruby 3+ no longer bundles it; `jekyll serve` needs it

# Windows doesn't ship timezone data
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
gem "wdm", "~> 0.1", platforms: [:mingw, :x64_mingw, :mswin]

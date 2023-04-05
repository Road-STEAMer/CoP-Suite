# frozen_string_literal: true

source "https://rubygems.org"

ruby RUBY_VERSION
DECIDIM_VERSION = { git: "https://github.com/decidim/decidim", branch: "release/0.27-stable" }

gem "decidim", DECIDIM_VERSION
# gem "decidim-consultations", DECIDIM_VERSION
# gem "decidim-initiatives", DECIDIM_VERSION
gem "redcarpet"

gem "bootsnap", "~> 1.4"

gem "puma", ">= 5.6.2"

gem "faker", "~> 2.14"
gem "uglifier", "~> 4.1"
gem "sprockets", "~> 3.7.2"



group :development, :test do
  gem "byebug", "~> 11.0", platform: :mri

  gem "decidim-dev", DECIDIM_VERSION
end

group :development do
  gem "letter_opener_web", "~> 2.0"
  gem "listen", "~> 3.1"
  gem "rubocop-faker"
  gem "spring", "~> 2.0"
  gem "spring-watcher-listen", "~> 2.0"
  gem "web-console", "~> 4.2"
end

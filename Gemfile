source 'https://rubygems.org'

gemspec

git 'https://github.com/anitagraham/refinerycms', branch: 'rails7' do
  gem 'refinerycms'

  group :development, :test do
    gem 'refinerycms-testing'
  end
end

gem 'refinerycms-i18n', git: 'https://github.com/anitagraham/refinerycms-i18n', branch: 'Rails7'

gem 'listen'

# Database Configuration
unless ENV['CI']
  gem 'activerecord-jdbcsqlite3-adapter', '>= 1.3.0.rc1', platform: :jruby
  group :development, :test do
  gem 'sqlite3', platform: :ruby
end
end

if !ENV['CI'] || ENV['DB'] == 'mysql'
  group :mysql do
    gem 'activerecord-jdbcmysql-adapter', '>= 1.3.0.rc1', platform: :jruby
    gem 'mysql2', platform: :ruby
  end
end

if !ENV['CI'] || ENV['DB'] == 'postgresql'
  group :postgres, :postgresql do
    gem 'activerecord-jdbcpostgresql-adapter', '>= 1.3.0.rc1', platform: :jruby
    gem 'pg', platform: :ruby
  end
end

group :development, :test do
  gem 'puma'
  gem 'pry-rails'
end

group :test do
  gem 'launchy'
  gem 'selenium-webdriver', require: false
end

# Refinery/rails should pull in the proper versions of these
group :assets do
  gem 'sass-rails'
  gem 'uglifier'
end

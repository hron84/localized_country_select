# encoding: UTF-8

require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

#load File.join(File.dirname(__FILE__), 'lib', 'tasks', 'localized_country_select_tasks.rake')

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the localized_country_select plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the localized_country_select plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'LocalizedCountrySelect'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README.rdoc')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

#
# Jeweler
#
begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "magic-localized_country_select"
    gemspec.summary = "Localized country select list"
    gemspec.description = "Localized country select list"
    gemspec.email = "mail@magiclabs.de"
    gemspec.homepage = "https://github.com/magiclabs/localized_country_select"
    gemspec.authors = ["LIM SAS", "Damien MATHIEU", "Julien SANCHEZ", "Hervé GAUCHER"]
    gemspec.add_dependency "hpricot", "~> 0.8"
  end
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end

require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "ging-opengraph"
    gem.summary = %Q{A very simple Ruby library for parsing Open Graph prototocol information from websites.}
    gem.description = %Q{A very simple Ruby library for parsing Open Graph prototocol information from websites. See http://opengraphprotocol.org for more information.}
    gem.email = "social-stream@dit.upm.es"
    gem.homepage = "http://github.com/ging/opengraph"
    gem.authors = ["Michael Bleigh", "Matt Wilson"]
    gem.add_dependency 'hashie'
    gem.add_dependency 'nokogiri', '~> 1.6.0'
    gem.add_dependency 'rest-client', '~> 1.8.0'
    gem.add_development_dependency "rspec", ">= 2.0.0"
    gem.add_development_dependency 'webmock'
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = 'spec/**/*_spec.rb'
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end

task :default => :spec

require 'rdoc/task'
RDoc::Task.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "opengraph #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

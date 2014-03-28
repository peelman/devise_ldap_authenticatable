require File.expand_path('spec/rails_app/config/environment', File.dirname(__FILE__))
require 'rdoc/task'

desc 'Default: run test suite.'
task :default => :spec

desc 'Generate documentation for the devise_ldap_authenticatable plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'DeviseLDAPAuthenticatable'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README.md')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "devise_ldap_authenticatable"
    gemspec.summary = "LDAP authentication module for Devise"
    gemspec.description = "LDAP authentication module for Devise"
    gemspec.email = "curtis.schiewek@gmail.com"
    gemspec.homepage = "http://github.com/cschiewek/devise_ldap_authenticatable"
    gemspec.authors = ["Curtis Schiewek", "Daniel McNevin", "Nick Peelman"]
    gemspec.add_runtime_dependency "devise", "~> 3.0.0"
    gemspec.add_runtime_dependency "net-ldap", "~> 0.3.1"
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

RailsApp::Application.load_tasks

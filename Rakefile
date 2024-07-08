# Rakefile

require 'rake/testtask'
require 'rdoc/task'

# Default task
task default: [:test]

# Task to clean up build artifacts
desc "Clean up build artifacts"
task :clean do
  sh "rm -rf build/*"
end

# Task to run tests
Rake::TestTask.new do |t|
  t.libs << "test"
  t.test_files = FileList['test/test_*.rb']
  t.verbose = true
end

# Task to generate documentation
RDoc::Task.new do |rdoc|
  rdoc.main = "README.md"
  rdoc.rdoc_dir = 'doc'
  rdoc.title = 'My Project Documentation'
  rdoc.options << '--all'
  rdoc.rdoc_files.include('README.md', 'lib/**/*.rb')
end
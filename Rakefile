require "bundler/gem_tasks"
require "rspec/core/rake_task"
require "rubocop/rake_task"
require "bundler/audit/task"

RSpec::Core::RakeTask.new(:spec) do |t|
  t.verbose = false
  t.rspec_opts = ["--format progress"]
end

RuboCop::RakeTask.new

Bundler::Audit::Task.new

task default: :spec
task default: :rubocop
task default: :"bundle:audit"

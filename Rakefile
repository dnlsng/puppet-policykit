require 'puppetlabs_spec_helper/rake_tasks'
require 'puppet-syntax/tasks/puppet-syntax'
require 'puppet-lint/tasks/puppet-lint'
require 'rspec-system/rake_task'

PuppetLint.configuration.send("disable_class_inherits_from_params_class")
PuppetLint.configuration.send("disable_80chars")
PuppetLint.configuration.ignore_paths = [
  'pkg/**/*.pp',
  'spec/**/*.pp',
  'tests/**/*.pp',
]

task :default => [
  :syntax,
  :lint,
  :spec,
]

guard :bundler do
  require 'guard/bundler'
  require 'guard/bundler/verify'
  helper = Guard::Bundler::Verify.new

  files = ['Gemfile']

  # Assume files are symlinked from somewhere
  files.each { |file| watch(helper.real_path(file)) }
end

guard 'nanoc' do
  watch('nanoc.yaml')
  watch('Rules')
  watch(%r{^(content|layouts|lib)/.*$})
end

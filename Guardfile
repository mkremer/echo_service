guard 'minitest' do
  watch(%r|^test/test_(.*)\.rb|)
  watch(%r|^lib/(.*)([^/]+)\.rb|)     { |m| "test/#{m[1]}test_#{m[2]}.rb" }
  watch(%r|^test/test_helper\.rb|)    { "test" }
end

guard 'process', :name => 'EchoService', :command => 'rackup', :stop_signal => "KILL"  do
  watch('echo_service.rb')
  watch('Gemfile.lock')
end

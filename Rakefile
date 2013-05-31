desc 'preview'
task :preview do
  server_start
end

def server_start
  require 'webrick'

  server = WEBrick::HTTPServer.new(
    {:BindAddress => '127.0.0.1',
      :DocumentRoot => '.',
      :Port => 4000})

  trap(:INT){server.shutdown}
  server.start
end

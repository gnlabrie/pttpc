task	:build do
     Dir.chdir("/tmp")
     puts "Building the package sir #{ENV['GO_PIPELINE_NAME']} #{ENV['GO_STAGE_NAME']} #{ENV['GO_JOB_NAME']} ..."
     sh "echo 'Hello' #{ENV['GO_PIPELINE_NAME']} #{ENV['GO_STAGE_NAME']} #{ENV['GO_JOB_NAME']} > 'hello.tmp'"
     puts "Working for 5 secs"
     sleep(5)
     puts "... Building complete "
end

task	:unit_test do
     Dir.chdir("/tmp")
     if ! File.exists("hello.tmp") then
          puts "File /tmp/hello.tmp missing"
          Fail
     else
          puts "File /tmp/hello.tmp exists"
     end
end

task	:package

def do_cmd(cmd)
    return_code = Kernel.system cmd
    raise "'#{cmd}' failed" unless return_code
end
task :default do
  return_code = 0
  Dir.chdir("test") do
    do_cmd 'ant debug install test -v'
  end
  do_cmd 'ant release -v'
end


task :default => "serve"

task :clean do
  sh "rm -rf _site"
end

task :serve do
  sh "jekyll --serve --auto"
end

task :deploy do
  sh "git push github github-master:master"
end

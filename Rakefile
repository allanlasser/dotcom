task :default => [:build]

task :build do
    sh "bundle exec jekyll build --config _config.yml"
end

task :serve do
    sh "bundle exec jekyll serve --config _config_dev.yml"
end


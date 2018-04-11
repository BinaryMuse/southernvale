desc "Clean _site"
task :clean do
  system "rm -r _site/*"
  puts "_site cleaned"
end

desc "Preview _site in a browser"
task :preview do
  system "bundle exec jekyll serve"
end

desc "Build _site"
task :build do
  system "bundle exec jekyll build"
end

desc "Sync _site"
task :sync do
  system "now ./_site -A ../now.json"
  puts "_site synced"
end

desc "Build and sync _site"
task :publish => [:build, :sync]

desc "Alias the latest build, making it public"
task :alias do
  system "now alias"
end

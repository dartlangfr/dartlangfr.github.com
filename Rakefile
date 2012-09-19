desc 'Running Jekyll with --server --auto options'
task :dev do
  system('jekyll --server --auto --future')
end

desc "Given a title as an argument, create a new post file"
task :new do
  title = ENV["title"] || "new-post"
  filename = "#{Time.now.strftime('%Y-%m-%d')}-#{title.gsub(/\s/, '-').downcase}.md"
  path = File.join("_posts", filename)
  if File.exist? path; raise RuntimeError.new("Won't clobber #{path}"); end
  File.open(path, 'w') do |file|
    file.write <<-EOS
---
layout: post
title: #{title}
date: #{Time.now.strftime('%Y-%m-%d %k:%M:%S')}
author: #{`git config --get user.email`.strip.chomp}
tags: misc
excerpt:
---
EOS
    end
    puts "Now open #{path} in an editor."
end

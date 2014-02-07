
puts Time.now.strftime("%Y-%m-%d")
task :new_post do
  require "highline/import"
  title = ask "Post title: "
  filename = title.downcase.gsub(' ', '_')

  File.open("_posts/#{Time.now.strftime("%Y-%m-%d")}-#{filename}.html", "w") do |f|
    f.write <<-EOF
---
layout: post
title: #{title}
data_key: #{filename}
---
    EOF
  end
  File.open("_data/#{filename}.yml", "w") do |f|
    f.write <<-EOF
---
- content: |
    Your first item
  terms:
    - A term beginners should learn

- content: |
    Your second item
  terms:
    - Another term for early-stage learners
    EOF
  end

end

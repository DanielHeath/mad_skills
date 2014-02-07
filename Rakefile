
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
<pre>Your first item</pre>

## Glossary
1. A simple term
2. Another simple term

<pre>Your second item</pre>

## Glossary
1. A simple term

    EOF
  end

end

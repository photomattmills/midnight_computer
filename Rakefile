task :new_post, [:post_name, :image_dir] do |t, args|
  time = Time.now
  date = time.strftime('%Y-%m-%d')
  slug = args.post_name.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '') #slug the title, to make a filemanmt

  file = File.open("_posts/#{date}-#{slug}.markdown", "w")
  file.puts <<-eom
---
layout: post
title: #{args.post_name}
date: #{time.strftime('%Y-%m-%d %H:%M:%S %z')}
---

<div class="center">
</div>
eom
  file.close
end

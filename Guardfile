# guard

ignore(/.bundle/)
ignore(/.config/)
ignore(/.gem/)
ignore(/.git/)
ignore(/.guard_history/)
ignore(/.idea/)
ignore(/.local/)
ignore(/.node-gyp/)
ignore(/.rspec_status/)
ignore(/Gemfile.lock/)
ignore(/node_modules/)

def print_line(character)
  puts "\n" + character * 80 + "\n"
end

watch(/.*\.js/) do |match|
  print_line("=")
  path = match[0]
  puts "Processing file: #{path}..."
  system "source ~/.bashrc; yarn eslint --fix #{path}; node scrap.js"
  puts "Done."
end

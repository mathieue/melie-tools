#!/usr/bin/env ruby

require 'optparse'

options = {}

opt_parser = OptionParser.new do |opt|
  opt.banner = "Usage: melie-find patterns [OPTIONS]"
  opt.separator  ""
  opt.separator  "Options"

  opt.on("-e","--edit","edit match files in vim") do |envrionment|
    options[:edit] = true
  end

  opt.on("-h","--help","help") do 
    puts opt_parser
  end
end

opt_parser.parse!

last = ARGV.pop
command="find -type d \\( -name .git -o -name .svn \\) -prune -o -type f -name \"*.pyc\" -prune -o -iname \"*#{last}*\" -print"

if !ARGV.empty?
  greps = ARGV.join(' | grep ') 
  command = "#{command} | grep #{greps}" 
end

if options[:edit]
  command="vim $(#{command})"
end

exec(command)

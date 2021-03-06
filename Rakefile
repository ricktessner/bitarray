require 'rake/rdoctask'
Rake::RDocTask.new do |rd|
  rd.main = "README"
  rd.rdoc_files.include("README", "LICENSE", "ext/*.c")
  rd.title = "BitArray Documentation"
  rd.rdoc_dir = "doc"
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "bitarray"
    gem.summary = "A bitarray class for Ruby, implemented as a C extension."
    gem.description = <<EOF
A bit array class for Ruby, implemented as a C extension. Includes methods for
setting and clearing individual bits, and all bits at once. Also has the
standard array access methods, [] and []=, and it mixes in Enumerable.
EOF
    gem.email = "ingramj@gmail.com"
    gem.homepage = "http://github.com/ingramj/bitarray"
    gem.authors = ["James E. Ingram"]
    gem.require_paths = ["ext"]
    gem.extensions = ["ext/extconf.rb"]
    gem.required_ruby_version = ">= 1.8.6"
    gem.rdoc_options << '--exclude=ext/Makefile' << '--exclude=ext/extconf.rb'
    gem.rdoc_options << '--title' << 'BitArray Documentation'
  end
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"
end


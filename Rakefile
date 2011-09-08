desc 'Delete symlink to *.local if any, and create new ones'
task :delete_symlinks do
  f1 = File.expand_path('~/.vimrc.local')
  f2 = File.expand_path('~/gvimrc.local')
  system 'rm ~/.vimrc.local' if File.exists?(f1)
  system 'rm ~/gvimrc.local' if File.exists?(f2)
  puts '*.local symlinks deleted!'
end
desc 'Create symlinks'
task :create_symlinks => :delete_symlinks do
  system 'ln -s ~/dotvim/vimrclocal ~/.vimrc.local'
  system 'ln -s ~/dotvim/gvimrclocal ~/.gvimrc.local'
  puts '*.local sylinks created!'
end
task :default => :create_symlinks

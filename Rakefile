namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'enters console'
task :console do
  Pry.start
end

desc 'Imports environment file'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migtates changes into database'
  task :migrate => :environment do
    Student.create_table
  end
  desc 'seeds db with dummy dats'
  task :seed do
    require_relative('./db/seeds.rb')
  end
end

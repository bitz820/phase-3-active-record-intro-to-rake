namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs wazzah to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
  
  desc "says hello in german to the terminal"
  task :moin do
    puts "moin wie gehts dir?"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc "Seed database with some dummy data"
  task seed: :environment do
    require_relative './db/seeds'
  end

end

task :environment do
  require_relative './config/environment'
end

desc "drop into pry console"
task console: :environment do
  Pry.start
end


task :environment do
  require_relative './config/environment'
end

desc 'drop into pry console'
task console: :environment do
  Pry.start
end

namespace :db do

  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end

end

namespace :greeting do

  desc "outputs 'hello from Rake' to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs 'hola de Rake' to the terminal"
  task :hola do
    puts 'Hola de Rake!'
  end

end

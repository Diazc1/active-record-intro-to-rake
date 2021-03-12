namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'ouputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end


#If you open up the Rakefile in this directory, you'll see our :hello task:

#Now, in your terminal in the directory of this project, type:
  #rake hello
  #you should see output of 'hello from Rake!'

#we need to give our Rake tasks descriptions. Let's give our hello task a description now:
  #desc 'outputs hello to the terminal'  -line2
    #Now, if we run rake -T in the terminal, we should see the following:
    #rake hello       # outputs hello to the terminal 





namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do    #This creates a task dependency
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end


  task :environment do 
    require_relative './config/environment'
  end


desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
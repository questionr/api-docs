namespace :deploy do
  def deploy(env)
    puts "Deploying to #{env}"
    if env == :vagrant
      system "VAGRANT_DEPLOY=true bundle exec middleman deploy"
    else
      system "bundle exec middleman deploy"
    end
  end

  task :vagrant do
    deploy :vagrant
  end

  task :production do
    deploy :production
  end
end

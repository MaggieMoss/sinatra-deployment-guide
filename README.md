# Deploy Sinatra Apps to Heroku
Steps for deploying a sinatra app to heroku

1. Create an account at heroku.com
2. In the terminal, run:
 * `$ heroku login`
 * `$ heroku create`

3. Back in the heroku dashboard:
  * Find the project that's been created for you, and click it.
  * Add an add-on for postgres: "Heroku Postgres"
  * Click it to view its details
  * Copy its URL (You’ll have to click a show button, it’ll be hidden) - it'll be a long string like: postgres://esfdizmindqtqp:W4B8yrM...
  * Edit your config/database.rb file to use this URL (~ line 9)

5. Run `bundle install`
6. Save your code using git:
 * a) `git status`
 * b) `git add -A`
 * c) `git commit -am "Readies app for deployment"`
7. Launch with: `git push heroku`
8. Create the database: `heroku run bundle exec rake db:migrate`


Links:
* https://devcenter.heroku.com/articles/rack

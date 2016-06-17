# sinatra-deployment-guide
Steps for deploying a sinatra app to heroku

1. Create an account at heroku.com
2. In the terminal, run:
 * `$ heroku login`
 * `$ heroku create`

3. Back in the heroku dashboard:
  * a) find the project that's been created for you, and click it.
  * b) Add an add-on for postgres: "Heroku Postgres"
  * c) Click it to view its details
  * d) Copy its URL (You’ll have to click a show button, it’ll be hidden) - it'll be a long string like: postgres://esfdizmindqtqp:W4B8yrM...
  * e) Edit your config/database.rb file to use this URL (~ line 9)

5. Run `bundle install`
6. save your code using git:
 * a) `git status`
 * b) `git add -A`
 * c) `git commit -am "Readies app for deployment"`
7. Launch with: `git push heroku`
8. Create the database: `heroku run bundle exec rake db:migrate`

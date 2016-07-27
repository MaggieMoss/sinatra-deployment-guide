# Deploy Sinatra Apps to Heroku
* Before deploying to heroku, you'll want to edit your Gemfile and your config/database.rb file. Use the examples in this repo as a guide. _NOTE: If you are deploying your finstagram app for the Intro to Web course your files should match exactly_


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
* https://devcenter.heroku.com/articles/git
* https://devcenter.heroku.com/categories/heroku-postgres
* http://www.sinatrarb.com/documentation.html

# Tips

Here are some important amendments / tips to read and follow as you go through the guide. If you skip these, your blog app may not work.

- When using the `rails new` command, the step where it runs `bundle install` for you automatically will take some time to complete. It may appear to be hung for some time (about 1 to 5 minutes). If so, go stretch, do a plank, or get coffee/tea while you wait.

- Immediately after creating the blog project with `rails new`, open the `Gemfile` in VS Code and update the line `gem 'sqlite3'` to `gem 'sqlite3', '1.3.13'`. Save the file and run `bundle` in the project directory. It should say something like `Fetching sqlite3 1.3.13 (was 1.4.1)`. If you do not follow this step, the app will complain that it cannot load/find the sqlite3 gem.

- When starting the Rails server using `bin/rails server` use the following command instead: `bin/rails server -b 0.0.0.0`. This will allow access to the app from our host machine. This is a Vagrant-specific nuance, which is why it's not mentioned in their guide.

- We suggest having two vagrant terminal tabs open, both within the blog application directory. That way you can have one running the server, and another to run other rails commands, as needed. This way you don't have to constantly start and stop the server. It will save you much time.

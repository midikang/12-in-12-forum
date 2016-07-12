== README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


Please feel free to use a different markup language if you do not plan to run
<tt>rake doc:app</tt>.

$ git remote add original https://github.com/midikang/12-in-12-forum.git
git push --set-upstream original master

rails g model post title:string content:text
     invoke  active_record
     create    db/migrate/20160712142831_create_posts.rb
     create    app/models/post.rb
     invoke    test_unit
     create      test/models/post_test.rb
     create      test/fixtures/posts.yml
admatoMacBook-Pro:forum ad$ rake db:migrate
== 20160712142831 CreatePosts: migrating ======================================
-- create_table(:posts)
  -> 0.0026s
== 20160712142831 CreatePosts: migrated (0.0027s) =============================

admatoMacBook-Pro:forum ad$ rails g controller posts
     create  app/controllers/posts_controller.rb
     invoke  erb
     create    app/views/posts
     invoke  test_unit
     create    test/controllers/posts_controller_test.rb
     invoke  helper
     create    app/helpers/posts_helper.rb
     invoke    test_unit
     invoke  assets
     invoke    coffee
     create      app/assets/javascripts/posts.coffee
     invoke    scss
     create      app/assets/stylesheets/posts.scss

admatoMacBook-Pro:forum ad$ rake routes
  Prefix Verb   URI Pattern               Controller#Action
   posts GET    /posts(.:format)          posts#index
         POST   /posts(.:format)          posts#create
new_post GET    /posts/new(.:format)      posts#new
edit_post GET    /posts/:id/edit(.:format) posts#edit
    post GET    /posts/:id(.:format)      posts#show
         PATCH  /posts/:id(.:format)      posts#update
         PUT    /posts/:id(.:format)      posts#update
         DELETE /posts/:id(.:format)      posts#destroy
    root GET    /                         posts#index

    admatoMacBook-Pro:forum ad$ git add .
    admatoMacBook-Pro:forum ad$ git commit -am ""
    Aborting commit due to empty commit message.
    admatoMacBook-Pro:forum ad$ git commit -am "Add post model & controller"
    [master 148a552] Add post model & controller
     13 files changed, 145 insertions(+), 28 deletions(-)
     create mode 100644 README.md
     delete mode 100644 README.rdoc
     create mode 100644 app/assets/javascripts/posts.coffee
     create mode 100644 app/assets/stylesheets/posts.scss
     create mode 100644 app/controllers/posts_controller.rb
     create mode 100644 app/helpers/posts_helper.rb
     create mode 100644 app/models/post.rb
     create mode 100644 db/migrate/20160712142831_create_posts.rb
     create mode 100644 db/schema.rb
     create mode 100644 test/controllers/posts_controller_test.rb
     create mode 100644 test/fixtures/posts.yml
     create mode 100644 test/models/post_test.rb

https://rubygems.org/search?utf8=%E2%9C%93&query=haml

haml, simple_form, devise

gem 'haml', '~> 4.0', '>= 4.0.7'
gem 'simple_form', '~> 3.2', '>= 3.2.1'
gem 'devise', '~> 3.2'

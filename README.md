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

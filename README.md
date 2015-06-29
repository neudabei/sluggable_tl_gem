### About

This gem allows you to build pretty 'sluggish' URLs for your Ruby on Rails apps.
So instead of `/1/post/2` your domains will read `/username/post-title`.


### Installation

1.) '$ gem install sluggable_tl'  
2.) '$ bundle install'  
3.) Restart your rails server  


### Configuration  

1.) Run a migration to create an extra column called `slug` formatted as string for all elements that require sluggish URLs
2.) In your respective model (e.g. the user model) include `include Sluggable
3.) Also in your model reference the column that you want to use to create slugs (e.g. `username` column in the user table or `title` column in the post model) 

```ruby
# user.rb

class User < ActiveRecord::Base
  include Sluggable

  sluggable_column :username # username must be a column in the user table corresponding to this model

# ... code omitted for brevity

end

```




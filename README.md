### About

This gem allows you to build pretty 'sluggish' URLs for your Ruby on Rails apps.
So instead of `/1/post/2` your domains will read `/username/post-title`.


### Installation

1. `$ gem install sluggable_tl`  
2. `$ bundle install`  
3. Restart your rails server  


### Configuration  

1. Run a migration to create an extra column called `slug` formatted as string for all elements that require sluggish URLs.  
2. In your respective model (e.g. the user model) `include Sluggable`  
3. Also in your model reference the column that you want to use to create slugs (e.g. `username` column in the user table or `title` column in the post model)  


```ruby
# user.rb

class User < ActiveRecord::Base
  include Sluggable

  sluggable_column :username # username must be a column in the user table corresponding to this model

# ... code omitted for brevity

end

```

### License

The MIT License (MIT)

Copyright (c) 2015 neudabei

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.  
  
*This project was created for a class at [gotealeaf.com](http://www.gotealeaf.com)* 
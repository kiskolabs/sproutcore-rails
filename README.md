SproutCore-Rails
================

SproutCore 2.0 for Rails 3.1.


Getting started
---------------

Add the gem to your application Gemfile:

    gem "sproutcore-rails"

Run `bundle install` and add the following line to 
`app/assets/javascripts/application.js`:

    //= require sproutcore

Ask Rails to serve HandlebarsJS templates to SproutCore
by putting each template in a dedicated ".js.hjs" file
(e.g. `app/assets/javascripts/templates/admin_panel.js.hjs`)
and including the assets in your layout:

    <%= javascript_include_tag "templates/admin_panel" %>

Bundle all templates together thanks to Sprockets,
e.g create `app/assets/javascripts/templates/all.js` with:

    //= require_tree .

Now a single line in the layout loads everything:

    <%= javascript_include_tag "templates/all" %>


License and Copyright
---------------------

Copyright (C) 2012 Kisko Labs Oy

Licensed under the MIT License. See the LICENSE file for details.

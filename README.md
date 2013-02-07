# facebox-rails

A gemified Facebox for Rails.

# Rails 3.1

Add it to your Gemfile:

    gem 'facebox-rails'

Include in your `app/assets/stylesheets/application.css`:

    /*
     * ...
     *= require jquery.facebox
     * ...
     */

And in `app/assets/javascripts/application.js`:

    //= require jquery.facebox

If you are using [turbolinks](https://github.com/rails/turbolinks), facebox will still think the necessary DOM objects are present after turbolink load. Avoid this by resetting the `inited` setting. 

    $(document).on 'page:change', -> $.facebox.settings.inited = false

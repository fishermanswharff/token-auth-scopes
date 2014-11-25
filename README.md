## Token Authentication with User Scopes

### Reading
* [comprehensive guide](http://railsapps.github.io/rails-authorization.html)
* [token auth without devise](http://www.brianauton.com/posts/token-authentication-devise.html)
* [Code School Blog on Token Auth](https://www.codeschool.com/blog/2014/02/03/token-based-authentication-rails/)
* [Sessions, Cookies, and Authentication](http://www.theodinproject.com/ruby-on-rails/sessions-cookies-and-authentication)


### Relevant Gems
* [Cancan](http://www.rubydoc.info/github/ryanb/cancan)
* [Warden](https://github.com/hassox/warden/wiki/Overview)
* [JWT](https://github.com/progrium/ruby-jwt)
* [Declarative Authorization](https://github.com/stffn/declarative_authorization)
* [sferik rails admin](https://github.com/sferik/rails_admin/wiki/Manually)
* [active admin](https://github.com/activeadmin/activeadmin)
* [Active Admin vs Rails Admin](http://www.slideshare.net/benoitbenezech/rails-admin-overbest-practices)

### Steps to add admins with a dashboard
Goal is to have token authentication with different roles: admins can do some things that users cannot.

Add to user model:

`enum role: [:admin, :employee]`

Generate migration

` rails g migration CreateDashboard`

Create dashboards_controller

In dashboards_controller, add `:before_action` 

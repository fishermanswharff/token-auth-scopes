## Token Authentication with User Scopes

* [sferik rails admin](https://github.com/sferik/rails_admin/wiki/Manually)
* [active admin](https://github.com/activeadmin/activeadmin)
* [Active Admin vs Rails Admin](http://www.slideshare.net/benoitbenezech/rails-admin-overbest-practices)
* [token auth without devise](http://www.brianauton.com/posts/token-authentication-devise.html)
* [Code School Blog on Token Auth](https://www.codeschool.com/blog/2014/02/03/token-based-authentication-rails/)
* [Sessions, Cookies, and Authentication](http://www.theodinproject.com/ruby-on-rails/sessions-cookies-and-authentication)


### Relevant Gems
* [Cancan](http://www.rubydoc.info/github/ryanb/cancan)
* [Warden](https://github.com/hassox/warden/wiki/Overview)
* [JWT](https://github.com/progrium/ruby-jwt)

### Steps to add admins with a dashboard
Goal is to have token authentication with different roles: admins can do some things that users cannot.

1. Add to user model:

`enum role: [:admin, :employee]`

2. Create nested routes:

`namespace :admin do`

`  resources :dashboards`

`end`

3. Generate migration

` rails g migration CreateDashboard`

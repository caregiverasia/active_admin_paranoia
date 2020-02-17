# active_admin_paranoia
This gem extends ActiveAdmin so that batch restore and batch archive actions will be available in resource index page. Also 'All' and 'Archived' scope will be available for resource index page. 'All' scope will show non archived resources and 'Archived' scope will show deleted or archived resources.

# This fork
Original version renames the Delete buttons/links of all the models in ActiveAdmin to Archive or whatever you specify 
in relevant translation file. This fork fixes it. The PR is created but looks like the author abandoned his repo.

# Installation
This gem assumes that you have already configured [paranoia](https://github.com/radar/paranoia) for you desire resource. Add this line to your application's Gemfile:

```ruby
gem "active_admin_paranoia", github: 'artemv/active_admin_paranoia', branch: 'global_delete_wording_intact'

```

And then execute:

    $ bundle

# Usages

```ruby
ActiveAdmin.register Post do
  active_admin_paranoia
  actions :all, :except => [:destroy]
end
```

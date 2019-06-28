---
layout: post
title:      "Biller CRUD App"
date:       2019-06-28 15:27:37 -0400
permalink:  biller_crud_app
---



<center> ![](https://www.freelogodesign.org/file/app/client/thumb/3572788b-93f9-4fbc-a179-add3c25c09b3_200x200.png?1560994314633)</center>


<center>***So What's behind Biller?***</center></p>

<center>The idea behind Biller is to come to a platform where all your bills are stored. Keep track of all your upcoming and past bills in a central location. </center> </p>

<center>![]( https://miro.medium.com/max/200/1*D07GoP9ZO3rXSVsVndX5kg.png)</center></p>

The structure is made to be very simple but very efficient. 

* Create Bills
* Read Bills                       
* Update Bills
* Delete Bills

Using Corneal gem to render my app structure steps:

Generate App Structure
```
corneal new APP-NAME
```

Run Bundle Install to install all essential gems:
```
cd APP-NAME
bundle install
```
Start your server with ```shotgun```:
```
shotgun
```
Create an MVC (Model View Controller) struction with migration file:
```
corneal scaffold NAME
```
The structure will display in your editor as follows:
```
└─app
  ├── controllers
  │   ├──application_controller.rb
  │   └──new_model_controller.rb
  ├── models
  │   └──new_model.rb
  └── views
      ├──new_models
      │  ├──index.html.rb.erb
      │  ├──show.html.rb.erb
      │  ├──new.html.rb.erb
      │  └──edit.html.rb.erb
      ├── layout.erb
      └── welcome.erb
```

<center> 

# Biller CRUD App</center>
**Controllers**

1. Application Controller:  Made up of several actions that are executed on request and then either it renders a template or redirects to another action. I've included actions/requests such as: creating a user, logging a user (Log In) in and signing a user out (Logout).
2. Bills Controller: Made up of several actions/request to render and redirect such as: **c**reating bills, **r**eading/viewing bills, **u**pdating/editing bills, **d**eleting/destroying bills.
3. Users Contoller: Made up of several actions/request to render and redirect such as:**c**reating users, **r**eading/viewing users profiles, **u**pdating/editing users profiles, **d**eleting/destroying users profiles.

**Models**
Represents  the data that is being transferred between the View and Controller components 
1. Bill.rb: Bills belong to users
2. User.rb: A user has many bills and has a secure password

**Views**
The visual representation of the inputs orchestrated by controllers and models. This is designed with ruby programming language, html, css, and forms.
1. Bills: Directory folder composed of several erb templates used to **create, read, update, delete** bills
2. Users: Directory folder composed of several erb templates used to **create, read, update, delete** users
3. Index: The landing page erb template welcomes users to the application
4. Layout: The design erb template composed of html and css used to design the view templates
5. Login: Langing page for signing into the application

**Config**
Built in settings to control which features are enabled
```
ENV['SINATRA_ENV'] ||= "development"

require 'bundler/setup'
Bundler.require(:default, ENV['SINATRA_ENV'])

ActiveRecord::Base.establish_connection(
  :adapter => "sqlite3",
  :database => "db/#{ENV['SINATRA_ENV']}.sqlite"
)


require_all 'app'

```

**db**
Holds database specific request
* Migrate: Allows you to alter your database in a structured manner so you can do things like
```
rake db:create              # Creates the database from DATABASE_URL or con...
rake db:create_migration    # Create a migration (parameters: NAME, VERSION)
rake db:drop                # Drops the database from DATABASE_URL or confi...
rake db:fixtures:load       # Load fixtures into the current environment's ...
rake db:migrate             # Migrate the database (options: VERSION=x, VER...
rake db:migrate:status      # Display status of migrations
rake db:rollback            # Rolls the schema back to the previous version...
rake db:schema:cache:clear  # Clear a db/schema_cache.dump file
rake db:schema:cache:dump   # Create a db/schema_cache.dump file
rake db:schema:dump         # Create a db/schema.rb file that is portable a...
rake db:schema:load         # Load a schema.rb file into the database
rake db:seed                # Load the seed data from db/seeds.rb
rake db:setup               # Create the database, load the schema, and ini...
rake db:structure:dump      # Dump the database structure to db/structure.sql
rake db:structure:load      # Recreate the databases from the structure.sql...
rake db:version             # Retrieves the current schema version number
```
 **config.ru**
config.ru (the .ru stands for "rackup") is a Rack configuration file with a list of instructions for rack which allows you to build web applications and work with requests and responses.

```
require './config/environment'


if ActiveRecord::Migrator.needs_migration?
  raise 'Migrations are pending. Run `rake db:migrate` to resolve the issue.'
end

use Rack::MethodOverride
run ApplicationController
use UsersController
use BillsController
```

To access the Biller App, here are the instructions
```
1. copy git repository: git@github.com:mtruman92/billers.git
2. In your terminal:  'git clone git@github.com:mtruman92/billers.git '
3. 'cd biller'
4. 'cd bills'
5. 'bundle install'
6. 'shotgun'
7. copy server address into browser and begin tracking your bills
```
</p>


<center>

## Happy Bill Tracking!

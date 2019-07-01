---
layout: post
title:      "Magic Behind Params Hash & Session Hash"
date:       2019-07-01 02:07:02 +0000
permalink:  magic_behind_params_hash_and_session_hash
---

# Params

Params is a hash of key/value pairs assigned to a variable called 'params'.  

Hashes are commonly used as a way to have named parameters in functions.
```

Dog.create(name: "Max", age: 10)

def self.create(params)
  @name = params[:name]
  @age  = params[:age]
end
```

Thanks to Sinatra, the params hash contains all the url and post parameters that are passed to your application. We can specifiy it in our controller and in our view to get values from the URL.

Example: If we hit a url like this:

```

http://localhost:4567/dogs?dogname=max&dogage=10

we would be able to call params[:dogname] to get the dogname

We can also create a route to match params. In our routes file, we might put something like:

get 'dogs/:id' => 'dogs#show'

We can then hit a URL like this:

/dogs/456
```

In the params hash, we now have an id. We can do params[:id] to get the value from the url.

# Sessions in Sinatra
We've all seen it in our browsers but whats the meaning behind HTTP? HTTP is an abbreviation for Hyper Text Transfer Protocol. It is an appliction layer protocol to convey information from the world wide web (www). HTTP protocol is a stateless and connectionless protocol. 

*What does that mean?*

Well, since HTTP is considered  a stateless protocol, each command that is requested  is executed independently, without prior knowledge of the requests that were executed before it. Each time you request a new route, all of the data in your application refreshes.

This is where the magic of sinatra sessions, like other web application tools, come in handy. To maintain data, we can use cookies which provide enough memory to store data between HTML transactions. Enabling sessions with sinatra allows us to store all of that data in cookies.  

Here’s an example below of how to enable sessions and then use the stored values across different routes:

```
require 'sinatra/base'

class SinatraApp < Sinatra::Base

enable :sessions

get '/welcome' do
  name = session[:name]
  "Hello, #{name}!"
end

post '/:name' do
  session[:name] = params[:name]
  redirect '/welcome'
end
end
```

In our get route, if we find something in session[:name], we will display it in the view. If nothing is stored on that key in the session then the view won’t display anything either.

In our post route we store the [:name] to the session hash.

When our browser is now redirected to GET the same URL again, it passes the cookie and since we have the :sessions feature enabled, Sinatra will decrypt and read the data, and put it back into the hash that is returned by the method session, so we can work with it.





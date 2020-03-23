---
layout: post
title:      "**Things to look out for and remember when coding in Ruby on Rails**"
date:       2020-03-23 15:44:19 +0000
permalink:  things_to_look_out_for_and_remember_when_coding_in_ruby_on_rails
---




**Partials and Locals**

When we’re coding out an application we’re always trying to keep our code dry(don’t repeat yourself) aka we want it non-repetitive. With that in mind we always end up putting code that we do need to repeat into a method like so: 

	def current_user
      @current_user ||= User.find_by(id: session[:user_id])
  end

This excerpt works to find or set a user’s info equal to our instance variable. We can save time, effort and computing power by making simple changes like so.

Now going a step further we can incorporate a partial into our code. First things first though we need to include a (_) in file name at the beginning to denote a partial. We usually use these for forms or things people need to fill in. So instead of typing our form into every section where it’s needed like so:

<%= form_for @funko_pop do |f| %>
  <ul>
  <% @funko_pop.errors.full_messages.each do |error| %>
    <li><%= error %></li>
  <% end %>
  </ul>
  <p>
    <%= f.label :title %><br/>
    <%= f.text_field :title %>
  </p>
  <p>
    <%= f.label :series %><br/>
    <%= f.text_field :series %>
  </p>
  <p>
    <%= f.label :description %><br/>
    <%= f.text_area :description %>
  </p>
    <p>
    <%= f.label :tag_list %><br/> 
      <%= f.text_field :tag_list %> 
   </p>  
   <p> 
    <% if @funko_pop.image.exists? %>
       <%= image_tag @funko_pop.image.url %><br/>
     <% end %>
     <%= f.label :image, "Attach a New Image" %><br/>
     <%= f.file_field :image %>
   </p>
  <p>
    <%= f.submit %>
  </p>
<% end %>

We can instead just call to render “insert file name ” in the spots where our form is needed.

<%= render 'form' %>

We can even add some customization into our partials by using locals when we call them. Ex:

<%= render partial: “form, locals: {zone: @zone}
By using locals we can dynamically insert custom variables into the form without actually hardcoding it in.

**Helper methods**

We use helper methods to keep our code dry but we sometimes put them in our views or controllers which can also leave a way for outside threats to threaten our code or critical information. A good way to combat this is too store those gold nuggets in your helper folders where your files can access them through inheritance.




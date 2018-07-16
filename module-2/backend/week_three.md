## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
* rails new project_name -T -db='postgresql' --skip-spring --skip-turbolinks

2. What do Models generally inherit from in rails?
* ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
* ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
* resources :horses, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?
* rake routes
* gives you prefix to a path helper, HTTP verb, uri, controller and action in that controller

6. What is an example of a route helper? When would you use them?
* horse_path(horse)
* use them to generate a uri

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* `_path` gives you uri, `_url` gives you the entire url

8. What are strong params and why are they necessary?
* strong params allow you to restrict/control information sent from forms to the database

9. What role does `form_for` play in helping us create our forms?
* they generate html for forms in our views

10. How does `form_for` know where to submit the user's input?
* by passing in the object from the controller

11. Create a form using a `form_for` helper to create a new `Horse`.

```
<%= form_for @horse do |f| %>

<%= f.label :name %>
<%= f.text_area :name %>

<%= f.submit %>
<% end %>
```

12. Why do we want to validate our models?
* to ensure valid data is saved in our database

13. What are the steps of the DNS lookup?
* a request is sent to a server and if it does not have the information, it sends a response of where to go next to look for this information
* many servers will be contacted until the full response is crafted for the resource.
* i will look this up to understand in better detail

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?

```ruby
class Horse
  def initialize(name)
    @name = name
  end

  def move
    prance
  end

  def prance
    "#{@name} prances"
  end
end

horse = Horse.new('Mr. Ed')
horse.move
```

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```

What is the different between how you would return true vs returning 3?

```ruby
furniture[:table][:height] == 3

furniture[:purchased] == true
```

16. What is inheritance?
* the concept of a child object acquiring state and behavior from a parent object
* a hierarchy of classes

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week

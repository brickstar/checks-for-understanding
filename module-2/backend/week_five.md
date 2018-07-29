### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
* you have to put something in application layout to be available to render throughout the app. i will have to look up the exact code
* then once that is in place you can use in controller
```
flash[:notice] = 'your pants are on fire'
```

2. Where is cart information/temporary information usually stored?
* sessions

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
* we want to persist for the life of the session, so the information is available for checkout as the user browses the rest of app
* maybe we want to keep a permanent cart for users, so they can access anytime they log in
4. What is the purpose of the asset pipeline?
* to wrap assets for easier and more efficient use in a production environment. eliminate white spaces and superfluous stuff
* to prepare and streamline the process of utilizing assets in our apps
* to
5. Why do we precompile our assets?
* see above
6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
```
* I assume the image_tag is a link to the image that follows in the string
* i would think the stylesheet_link_tag links to some external css
* and javascript_include_tag links to javascript assets, but not sure
* we haven't learned about these in class, i will research

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
* how to install your app
* what tech it is using
* lists the purpose of the app
* lists what problems it solves, what it does (kind of like above)
* gems and what they do?

8. What are the top four accessibility issues that we as developers should be aware of?
* i have no idea, we haven't touched in class. will research

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
* this is a callback. i've seen them used in controllers to dry up code that is used in more than one action
* maybe before save would be in the model?

10. Given the following object, how would we create a scope for all users who are active?
* no idea, will have to research
```ruby
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?
* class operates on entire collection, scope operates on a selected portion of the collection.
* we didn't learn anything about scope yet so not sure?

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

thing = {cart: {"17" => 4, "204" => 52, "29" => 22}}
thing[:cart]['48'] = 4

  12a. How would you add item with id of 48 with a quantity of 4?  
  ```
  thing = {cart: {"17" => 4, "204" => 52, "29" => 22}}
  thing[:cart]['48'] = 4
  ````

  12b. How would you increase the quantity of item 29?  
  ```
  thing[:cart]['29'] += 1
  ```
  12c. How would you find out how many items your user is thinking about purchasing?   
  ```
  thing[:cart].values.sum
  ```

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
* not sure, have to research

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
```
use gsub and regex
```


### Self Assessment:
Choose One:
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel comfortable with the content presented this week

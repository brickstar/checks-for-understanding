## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
* GET - receive a resource
* POST - create a resource
* PUT - update an entire resource
* PATCH - update part of a resource
* DELETE - delete a resource

2. What is Sinatra?
* a domain specific language and ruby-based web application framework

3. What is MVC?
* A design pattern used by Rails. Also used by Turing for our Sinatra LittleShop app :)
* Model - interacts with database
* View - renders the resource in the browser
* Controller - the traffic cop between the model and view

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
* For readability, maintainability, scalability and RESTfulness

5. What types of variables are accessible in our view templates without explicitly passing them?
* instance variables

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses' do
    name = 'Mr. Ed'
    erb :index, locals: { name: name }
  end
  ```

8. What's the purpose of ERB?
* to embed ruby code in html - to be executed or inserted into our application views

9. Why do I need a development AND test database?
* to interact with our database structure without altering the data itself.
* a clear delineation between our app's expected/intended behavior with a resource, and the actual behavior our app has with our resources

10. What is CRUD and why is it important?
* Create, Read, Update, Destroy
* Allows us to interact with resources in our applications

11. What does HTTP stand for?
* hypertext transfer protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

  ```erb
  <%= inserts a value %> = is the echo operator
  <% executes code but does not insert the value %>
  ```

13. What's an ORM? What does it do?
* Object Relational Mapper
* Allows us to interact with resources in object oriented programming languages

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
* ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

* get '/restaurants' shows all restaurants
* get '/restaurants/:id' shows one restaurant
* get '/restaurants/new' render a form to create a restaurant
* post '/restaurants' creates a restaurant
* put '/restaurants/:id' edits a single restaurant
* delete '/restaurants/:id' deletes a restaurant
* get '/restaurants/edit' render a form to update a restaurant

16. What's a migration?
* a way to make changes to our resources

17. When you create a migration, does it automatically modify your database?
* No

18. How does a model relate to a database?
* it directly interacts with our resources

19. What is the difference between `#new` and `#create`?
* new returns an object but create will return and save it to the database

### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?

  ```ruby
  require './app/models/film.rb'

  CSV.foreach('./data/films.csv', :headers => true, header_converters: :symbol) do |film|
      Film.create(film.to_h)
  ```

21. Given the following hash:

  ```ruby
  activities = {
    hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
    karaoke: {cost: $10, supplies: ['courage', 'microphone']},
    brunch: {cost: $35, supplies: ['mimosa flutes']},
    antiquing: {cost: $200, supplies: ['list of antique stores']}
  }
  ```
How would I add 'granola bar' to things you should have when hiking?

  ```ruby
  activities[:hiking][:supplies] << 'granola bar'
  ```

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.

### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week

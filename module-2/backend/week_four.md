## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
* pieces of information stored locally on your machine that communicate with websites

2. What’s the difference between a session and a cookie?
* cookies are stored locally on a user's computer, sessions are stored on a server

3. What’s a flash and when do you want to use flashes?
* alert messages rendered before or after actions on a site
* can be used to warn people of consequences of an action, or to convey information about whether or not an action was successful

4. Why do people say “HTTP is stateless”?
* each request and response knows nothing of the one before

5. What’s authentication? Explain.
* authentication is who you are - how you are defined as a user

6. What’s the difference between authentication and authorization?
* authentication refers to who you are, authorization refers to what you are allowed to do

7. What’s a before filter?
* i think it's like a before_action - something that is executed before an action in a controller

8. How do we keep track of a user once they’ve logged in?
* session

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
* namespacing a resource allows to filter out certain user types from accessing parts of an application
* nesting is used to build pathing and also passes information through the route

10. At a high level, what tools can you use to implement authorization? How would you use them?
* namespacing, you can set a before_action to filter out default users

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
* allows you to convert integer roles in database to strings
* integer
* declared in the model

12. What are some strategies you can use to keep your views DRY?
* partials

### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```

```ruby
puts given.map { |hash| hash[:holiday][:name] }.sort
```
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

```ruby
thing = "$300"
thing.split('').shift.to_i

thing = "$300"
thing.gsub(/[$]/, '').to_i

thing = "300.0"
thing.to_i
```
* i am sure there is a better way to do this - if not gsub with regex pulling out as much as you can, then there is method already in a library for this
* what is the best practice for this?

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

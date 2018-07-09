## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
* ActiveRecord allows us to map table columns to corresponding object attributes and wrap them into ruby objects. It gives us methods that exercise business data logic - methods that generate SQL queries that interact with relational databases

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
* where, find, find_by, where.not, select, joins, order, group, includes, references, limit
* we have access to them by inheriting from ActiveRecord::Base

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
* team = Team.find(4).name
* Owner.find_by(team: team)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
* Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
* many to many - at Turing for example, a teacher has many students and a student has many teachers

6. Define foreign key, primary key, and schema.
* primary key - id auto-incremented to identify rows in a primary table
* foreign key - id in a belongs_to that relates the table corresponding table that has_many
* schema - a blueprint or representation of the tables in a database

7. Describe the relationship between a foreign key on one table and a primary key on another table.
* the primary key of the has_many links to the foreign key of the belongs_to

8. What are the parts of an HTTP response?
* headers
* body
* status code

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
* average - calculates the average of passed parameter
* sum - calculates the sum of the passed parameter
* where - returns all the things that are passed into the parameter
* order - returns a sorted collection
* joins - creates a temporary table between attributes of two existing tables in the database

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
* rake db:create - creates the development and test databases
* rake db:migrate - uses generated migrations to change the database
* rake db:rollback - sets the database back to it's state prior to the previous db:migrate

3. What two columns does `t.timestamps null: false` create in our database?
* created_at
* updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
* at Turing a school has_many teachers and a teacher belongs_to a school (unless some of you currently teach someplace else)

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
* teachers table has an id, name and a school_id.
* schools table has a name and an id that links to school_id on the teachers table

6. Give an example of when you might want to store information besides ids on a join table.

7. Describe and diagram the relationship between patients and doctors.
* a doctor has_many patients and a patient has_many doctors

8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
* if views or parts of a view are used in several places

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week

## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  * ActiveRecord is a library for working with relational databases
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  * Team.all, Team.first, these methods are inherent in AR
3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  * Team.find_by_id(4), Team.find_by_id(4).name
4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  * Team.find_by_id(4).owner
5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  * the students table will have a foreign key relating to the primary key of the teachers table, teacher_id.
6. Define foreign key, primary key, and schema.
  * foreign key is an integer on one table that refererences the primary key of another table. primary key is the id of a table, all of which will be unique. a schema is a representation of relations between tables and elements in those tables
7. Describe the relationship between a foreign key on one table and a primary key on another table.
  * a foreign key on one table is specifically referencing a primary key on another
8. What are the parts of an HTTP response?
  *

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?

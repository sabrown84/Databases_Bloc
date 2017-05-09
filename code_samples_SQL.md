Remove Duplicates in Query
  * Post.where.title.is_uniq?
  * SELECT DISTINCT title * FROM posts;
Filter records using inequalities, pattern matching, ranges, and boolean logic
  * Post.where.id < 3
  * SELECT * FROM posts WHERE id < 3;
  * Post.where.rating < 6
  * SELECT * FROM posts WHERE rating < 6;
  * Post.where.published = true
  * SELECT * FROM posts WHERE published = true;
Sort records in a particular order
  * Post.sort_by(id)
  * SELECT * FROM posts ORDER BY id ASC;
Limit the number of records returned
  * Post.all.limit(3)
  * SELECT * FROM posts LIMIT 3;
Group records into sections
  * Post.all.rating.sort(author)
  * SELECT rating FROM posts GROUP BY author;
Perform calculations using aggregate functions
  * Post.all.sum(rating)
  * SELECT * FROM posts JOINT categories ON posts.posts_category = post.category;
Join Tables
  - Inner
    * Post.all.merge(cargories, post.category)
    * SELECT * FROM posts JOIN categories ON posts.posts_category = post_category;
  - Cross
    * Post.title && Post.author && Category.post  
    * SELECT posts.title, posts.author, categories.post FROM posts, categories;
  - Outer
    * Post.all.merge(users, post.author)
    * SELECT * FROM posts LEFT JOIN users ON post.author = author.name

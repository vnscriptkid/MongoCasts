# MongoCasts

- update many records:
  - **naive**: fetch many to server, then update each
  - better: use update operator https://docs.mongodb.com/manual/reference/operator/update/

- join alternative op in mongo:
```js
User.findOne({ name: 'Joe' })
      .populate('blogPosts');
// these are 2 ops behind the scene: (2 round trips to db)
// - trip 1: get user
// - trip 2: get posts
```
  
- avoid cyclic imports:
```js
// import BlogPost from 'models/BlogPost';
mongoose.model('BlogPost')
```

- types of operators:
  - update
  - query

- fulltext search
  - index first
  - `$text`
  - partial search works on stem word

Eloquent Relationships
===
###### tags: `laravel` `eloquent` `models` `relationships` `one-to-many` `many-to-many` 

# Eloquent


###### Hint : hasOne, hasMany, belongsTo all use same attributes: Model, foreign_key, local_key.

### One to One
==Target | fk | local_key==
```php
  return $this->hasMany('App\Comment', 'comment_id', 'id');
```

### One To Many
==Target | fk | local_key==
```php
  return $this->hasMany('App\Comment', 'comment_id', 'id');
```

### BelongsTo
###### Inverse of One to Many and One to One
==Model | fk | parent_pk==
```php
    return $this->belongsTo('App\Post', 'post_id', 'id');
```
### Many To Many
==Target Class | Join table | Fk join 2 Source | fk join 2 target==
```php
    return $this->belongsToMany('App\Post', 'user_posts', 'user_id', 'post_id');
```
Database
====

# table list
- users
| column  |   type   |
|:-------:|:--------:|
|id       |integer   |
|name     |string    |
|email    |string    |
|password |string    |
|avatar   |string    |
|member   |string    |
|profile  |text      |
|works    |string    |

- prototypes
|  column  |  type  |
|:--------:|:-------:|
|id        |integer  |
|title     |string   |
|catch_copy|string   |
|concept   |string   |
|user_id   |integer  |
|prototype_id|integer|


- comments
|  column  |  type  |
|:--------:|:---------:|
|id        |integer    |
|text      |text       |
|user_id   |integer    |
|prototype_id|integer  |

- likes
|  column  |  type  |
|:---------:|:--------:|
|id         |integer   |
|prototype_id|integer  |
|user_id    |integer   |

- images
|  column  |  text  |
|:--------:|:-------:|
|id        |integer |
|prototype_id|integer|
|image     |string  |
|role      |string  |


## Tables
### Users
|column|type|
|:---:|:---:|
|name|string|
|group|string|
|profile|string|
|avatar|string|
|works|string|

### Prototypes
|column|type|
|:---:|:---:|
|name|string|
|user_id|integer|
|catch_copy|string|
|concept|string|
|like_count|integer|
|image|string|

### Comments
|column|type|
|:---:|:---:|
|user_id|integer|
|prototype_id|integer|
|text|text|

### Images
|column|type|
|:---:|:---:|
|prototype_id|integer|
|status|integer|
|profile|string|

### Likes
|column|type|
|:---:|:---:|
|user_id|integer|
|prototype_id|integer|

# Association

### Users
|association|table|
|:---:|:---:|
|has_many|prototypes|
|has_many|comments|

### Prototypes
|association|table|
|:---:|:---:|
|belongs_to| user |
|has_many |comments|
|has_many |likes|
|has_many |images|

### Comments
|association|table|
|:---:|:---:|
|belongs_to|prototype|
|belongs_to|user|

### Likes
|association|table|
|:---:|:---:|
|belongs_to|prototype|
|belongs_to |user|

### Images
|association|table|
|:---:|:---:|
|belongs_to|prototype|

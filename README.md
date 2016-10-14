Database
====

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
- has_many :prototypes
- has_many :comments

### Prototypes
- belongs_to :user
- has_many :comments
- has_many :likes
- has_many :images

### Comments
- belongs_to :prototype
- belongs_to :user

### Likes
- belongs_to :prototype
- belongs_to :user

### Images
- belongs_to :prototype

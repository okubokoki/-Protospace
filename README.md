Database
====

#table list
users
prototypes
comments
likes
images

# Users

## column
- id :integer
- name :string
- email :text
- password :string
- avatar :text
- member :string
- profile :text
- works :text

## associations
has_many :prototypes
has_many :comments



# Prototypes

## column
- id :integer
- title :string
- catch_copy :text
- concept :text
- user_id :integer
- prototype_id

## association
belong_to user
has_many :comments
has_many :likes
has_many :images

# Comments

## column
- id :integer
- comment :text
- user_id :integer
- prototype_id :integer

##associstions
belong_to :prototype
belong_to :user

# Likes

##column
- id :integer
- prototype_id :integer
- user_id :integer

## associations
belong_to :prototype
belong_to :user

# Images

## column
- id :integer
- prototype_id :integer
- image

# associations
belong_to :prototype

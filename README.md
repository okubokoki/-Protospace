Database
====

#table list
- users
- prototypes
- comments
- likes
- prototypeimages

# Users

## column
- id :integer
- name :string
- email :string
- password :string
- avatar :string
- member :string
- profile :text
- works :string

## associations
- has_many :prototypes
- has_many :comments



# Prototypes

## column
- id :integer
- title :string
- catch_copy :string
- concept :string
- user_id :integer
- prototype_id :integer

## association
- belongs_to :user
- has_many :comments
- has_many :likes
- has_many :images

# Comments

## column
- id :integer
- text :text
- user_id :integer
- prototype_id :integer

##associstions
- belongs_to :prototype
- belongs_to :user

# Likes

##column
- id :integer
- prototype_id :integer
- user_id :integer

## associations
- belongs_to :prototype
- belongs_to :user

# Prototypeimages

## column
- id :integer
- prototype_id :integer
- image :string
- role :string

# associations
- belongs_to :prototype

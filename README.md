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
- name :text
- email :text
- password :text
- avatar :string
- member :text
- profile :string
- works :text

## associations
- has_many :prototypes
- has_many :comments



# Prototypes

## column
- id :integer
- title :string
- catch_copy :text
- concept :text
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

Database
====

#table list
- users
- prototypes
- comments
- likes
- images

# Association

## Users
- has_many :prototypes
- has_many :comments

## Prototypes
- belongs_to :user
- has_many :comments
- has_many :likes
- has_many :images

## Comments
- belongs_to :prototype
- belongs_to :user

## Likes
- belongs_to :prototype
- belongs_to :user

## Images
- belongs_to :prototype

# column

## Users
- id :integer
- name :string
- email :string
- password :string
- avatar :string
- member :string
- profile :text
- works :string

## Prototypes
- id :integer
- title :string
- catch_copy :string
- concept :string
- user_id :integer
- prototype_id :integer

## Comments
- id :integer
- text :text
- user_id :integer
- prototype_id :integer

## Likes
- id :integer
- prototype_id :integer
- user_id :integer

## Images
- id :integer
- prototype_id :integer
- image :string
- role :string
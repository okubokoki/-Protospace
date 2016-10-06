# Protospace
====

## User

### association
has_many Prototypes

### column
- id
- email
- avatar
- created_at
- updated_at

## Prototype

### association
belongs_to user

### column
- content
- user_id
- prototype_id
- created_at
- updated_at


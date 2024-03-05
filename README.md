bill-split
Design
Actors:

User
System
Models:

User -- name, email
Group -- name, members
Bill -- amount, title, created_by, splits
Split -- bill, split_amount, user_id, percentage, share
APIs:

register_user(email, name) -> id
create_goup(name, creator_id) -> id
add_user(group_id, user_id) -> id
create_bill(amount, title, splits: List[Split])
list_splits(user_id, group_id)
settle(user_id, friend_id)
get_balance(user_id)
Keeping out of scope for now:

Editing an existing bill
Group simplify balances
Using decimal type for currency instead of float, error margin taken as 0-1
Setup proper logger
Authentication and authorization for apis

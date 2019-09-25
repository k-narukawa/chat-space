# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
## userテーブル

|Column|Type|Options|
|id|integer|null: false, foreign_key: true|
|nickname|string|null: false|
|email|string|unique,null: false|
|password|string|null: false|	


## groupテーブル

|id|integer|null: false, foreign_key: true|
|groupname|string|null: false|



# groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user	

## messagesテーブル
|Column|Type|Options|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|message|text|
|image|string|

### Association
- belongs_to :group
- belongs_to :user	





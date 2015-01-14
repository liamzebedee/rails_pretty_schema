# rails_pretty_schema
Parses schema.rb and outputs a nicer pretty schema

## Example
Takes a schema file containing Ruby code like this:
```
  create_table "gigs", force: true do |t|
    t.decimal  "cost",           default: 0.0
    t.datetime "start_datetime"
    t.string   "name",           default: ""
    t.datetime "created_at"
    t.datetime "updated_at"
    t.boolean  "moderated",      default: false
    t.boolean  "approved",       default: false
    t.text     "link_to_source", default: ""
    t.integer  "venue_id"
    t.text     "description",    default: ""
    t.datetime "end_datetime"
    t.boolean  "eighteen_plus"
  end

  create_table "instagram_apis", force: true do |t|
    t.integer  "new_media_count"
    t.integer  "last_seen_instagram_id"
    t.datetime "created_at"
    t.datetime "updated_at"
  end
```

and outputs a pretty version looking like this:
```
gigs
	cost
	start_datetime
	name
	created_at
	updated_at
	moderated
	approved
	link_to_source
	venue_id
	description
	end_datetime
	eighteen_plus
instagram_apis
	new_media_count
	last_seen_instagram_id
	created_at
	updated_at
```

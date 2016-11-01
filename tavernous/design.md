### Components
Admin Panel
Users
Tables
Event (Convention,Gameday)

### Routes

	/users/
	/tables/
	/event_id/tables

### Models

_TableTypes_
	
	event
	stand_alone
	recurring

_Table_

	belongs_to: event
	belongs_to: owner (user)
	has_many: gamemasters (user)
	has_many: players (user)
	has_many: watchers (user)
	integer: max_seats
	string: name
	text: description
	date_time: start
	date_time: end
	weekdays: recurring_days

_User_

	boolean: is_admin
	has_and_belongs_to_many: events
	has_many: tables

_Event_

	has_many: tables

_OrganizedPlay_

	AdventurersLeague
	PathfinderSociety
	GreyhawkReborn
	ShadowrunMissions
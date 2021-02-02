 # FOMO-NOMO! 
![](images/home-page-copy.png)
 ---

## How to Set Up:
1. Fork & Clone
2. Install dependencies
```
npm i
```

## [Link to Frontend Repo](https://github.com/SFX818/Team-5-frontend)
## [Link to Deployed Heroku Backend](https://fomo-nomo-backend.herokuapp.com/)

---

## Concept:

The FOMO NOMO App is for the user who is bored at home and is looking for new virtual events to avoid the FOMO. Users can add events to their personal calendar or coordinate attending events with their friends.


## Technologies Used:

* Node / Express
* Mongoose
* MongoDB
* Axios

## Approach:

### RESTful Routes: 

| Route | HTTP Verb | CRUD | Model | Explanation			
| ------------- | ------------- | ------------- | ------------- | ------------- |	
| `"/api/auth/signup"` ✅| POST | CREATE | `user` | Post a new user to database
|`"/api/auth/signin"` ✅| POST | CREATE | `user` | Get user from database
|`"/profile/myevents"` ✅| GET | READ | `event` | Gets user's saved events
|`"/profile/myevents/addevent"`✅ | POST | CREATE | `event` | Saves event to user's calendar
|`"/profile/myevents/:id"` ✅| DELETE | DELETE | `event` | Deletes event from user's calendar
|`"/events/comments/:id"` ✅| GET | READ | `event` & `comment` | See comments for event id
|`"/getComment/:id"` ✅| GET | READ | `event` & `comment` | Get single comment for event id (used for update)
|`"/events/newcomment/:id"` ✅| POST | CREATE | `event` & `comment` | Save comment to event id
|`"/events/comment/:id"` ✅| DELETE | DELETE | `event` & `comment` | Delete comment from event id
|`"/events/updatedcomment/:id"` ✅| PUT | UPDATE | `event` & `comment` | Update comment for event id



<br/>


---

<br/>

## General Approach:

Our team worked on the backend first to establish our routes and determine how information will be saved in the database. We tested all of our routes in Postman first to verify data can be saved to our database collections.

Following testing in the database, we created the frontend in order to send data back to the backend database. This required services on the frontend to hit our routes and execute functions hosted in our controllers.

<br/>

---

<br/>

## Challenges:
- Adding events to user's calendar
- Saving frontend API data to backend
- Associating comment to user and event

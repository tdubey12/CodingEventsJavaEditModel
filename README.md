The coding event app consist of event,eventcategory ,tag.

This consist of controller,model,view,data classes.

I will add Person class which holds the following fields:

id (int) - the unique user ID
firstName (String) - the user’s first name
lastName (String) - the user’s last name
email (String) - the user’s email, which will also function as their username
password (String) - the user’s password
The class would need getters for all of these fields. It could have setters for all fields except id (since it shouldn’t change). I will use AbstractEntity and extends the Person class to get the id field.

The Person class will also have the following references:

PersonProfile - a class to gather up all of the profile information about the user, this would be one-to-one relation.
List<Events> eventsAttending - to store events the user wants to attend ,this would be many-to-many relation.
List<Events> eventsOwned - a different list, to store the events the user has created ,this would be one-to-many.
Person would have a many-to-many relationship with Event via List<Events> eventsAttending. It would have a one-to-many relationship with Event via List<Events> eventsOwned.

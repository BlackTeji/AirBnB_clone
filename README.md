#HBNB - The Console

##Holberton AirBnB Clone project

This is the first portion of a project to build a clone of the AirBnB website. The first goal of this project is to create a program that serializes and deserializes objects into json files, and reloads them on startup for use between sessions, or in other words making the data persist between sessions.

The second goal of the project is to build a console to manage all this stored data. The console is made to update, delete, and create new instances of any class of data. It also keeps track of when the objects it has made were created, and updated.

#General Use

#First clone this repository.

Once the repository is cloned locate the "console.py" file and run it as follows
/AirBnB_clone$ ./console.py
#When this command is run the following prompt should appear:
(hbnb)

This prompt designates you are in the "HBnB" console, there are a variety of commands available once the console program is run.
Commands

* create - Creates an instance based on given class

* destroy - Destroys an object based on class and UUID

* show - Shows an object based on class and UUID

* all - Shows all objects the program has access to, or all objects of a given class

* update - Updates existing attributes an object based on class name and UUID

* quit - Exits the program (EOF will as well)

- It is possible to call <class_name>.<command>(arguments) as well
Examples
Example 0: Create an object
Usage: create <class_name>

(hbnb) create BaseModel
(hbnb) create BaseModel
3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb)                   
Example 1: Show an object
Usage: show <class_name> <class_id>

(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc-efb6-4041-bfe9-3cc9727588f8', 'created_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96959), 
'updated_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96971)}
(hbnb)  
Example 2: Destroy an object
Usage: destroy <class_name> <class_id>

(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
** no instance found **
(hbnb)   
Example 3: Update an object
Usage: update <class_name> <class_id>

(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) show BaseModel b405fc64-9724-498f-b405-e4071c3d857f
[BaseModel] (b405fc64-9724-498f-b405-e4071c3d857f) {'id': 'b405fc64-9724-498f-b405-e4071c3d857f', 'created_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729889), 
'updated_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729907), 'first_name': 'person'}
(hbnb)

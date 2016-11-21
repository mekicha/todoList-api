A simple Rest Api for a todo list app with basic authentication.

Following a tutorial from:
https://blog.miguelgrinberg.com/post/designing-a-restful-api-with-python-and-flask

To run
------
== clone the repo
== cd to the directory
== python app.py
==open another terminal and run the following:

curl -i http://localhost:5000/todo/api/v1.0/tasks 
curl -i http://localhost:5000/todo/api/v1.0/tasks/2
curl -i -H "Content-Type: application/json" -X POST -d '{"title":"Read a book"}' http://localhost:5000/todo/api/v1.0/tasks
$ curl -i -H "Content-Type: application/json" -X PUT -d '{"done":true}' http://localhost:5000/todo/api/v1.0/tasks/2

I have protected the http://localhost:5000/todo/api/v1.0/tasks as an example to show authentication. So you'll need to 
curl -u mekicha:python -i http://localhost:5000/todo/api/v1.0/tasks instead to get the result

TO DO:
------
Add database support
Add query filters
Support handling multiple users
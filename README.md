Installation
------------
$ virtualenv venv
$ source venv/bin/activate
(venv) $ pip install -r requirements.txt


Running
-------
(venv) $ python api.py
* Running on http://127.0.0.1:5000/
* Restarting with reloader

Usage
-------
$ curl -i -X POST -H "Content-Type: application/json" -d '{"username":"rahul","password":"ranjan"}' http://127.0.0.1:5000/api/users
    
    {
      "username": "rahul"
    }


$ curl -u rahul:ranjan -i -X GET http://127.0.0.1:5000/api/resource
    
    {
      "data": "Hello, rahul!"
    }


$ curl -u rahul:ranjan -i -X GET http://127.0.0.1:5000/api/token
    
    {
      "duration": 600,
      "token": "eyJhbGciOiJIUzI1NiIsImV4cCI6MTM4NTY2OTY1NSwiaWF0IjoxMzg1NjY5MDU1fQ.eyJpZCI6MX0.XbOEFJkhjHJ5uRINh2JA1BPzXjSohKYDRT472wGOvjc"
    }
    

$ curl -u eyJhbGciOiJIUzI1NiIsImV4cCI6MTM4NTY2OTY1NSwiaWF0IjoxMzg1NjY5MDU1fQ.eyJpZCI6MX0.XbOEFJkhjHJ5uRINh2JA1BPzXjSohKYDRT472wGOvjc:x -i -X GET http://127.0.0.1:5000/api/resource
    
    {
      "data": "Hello, rahul!"
    }

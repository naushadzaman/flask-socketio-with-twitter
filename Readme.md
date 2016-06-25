This code shows the real time streaming of tweets with Flask and StreamIO to your apps, after doing some processing on your backend. So it flows as follows in realtime. 
Twitter -- (TwitterStreaming) --> YourBackend -- (Flask/StreamIO) --> YourFrontend

YourBackend -- (Flask/StreamIO) --> YourFrontend part code is taken (after stripping off the listening part, so kept only one way communication codes from server to client) from very helpful tutorial by Miguel Grinberg on the topic:  http://blog.miguelgrinberg.com/post/easy-websockets-with-flask-and-gevent
with accompanying github repo: https://github.com/miguelgrinberg/Flask-SocketIO

I added Twitter -- (TwitterStreaming) --> YourBackend part to accompany rest of the codes. There could be a better way of doing it. Suggestions are very welcome. 

You have to add twitter credentials in the cred parameter in app.py. Also to test other keywords, change the list _keywords. 

# Setup the virtual environment 
$ virtualenv --dist venv
$ source venv/bin/activate
$ pip install -r requirements.txt 

OR 
# If you don't want virtualenv
$ sudo pip install -r requirements.txt

# Run the server
$ python app.py 

# Checkout the output in the browser. 
http://127.0.0.1:5000
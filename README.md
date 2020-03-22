# Python-gunicorn-Heroku
Deploying python app on Heroku using gunicorn


Normally, Flask is run in single-threaded mode, and can only handle one request at a time, and any parallel requests should wait until they can be handled. Solving this problem is a quite easy work to do, you only need put threaded=True                                                                                                                                       app.run(port=2020,threaded=True)

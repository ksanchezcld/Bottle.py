Bottle.py
=========

  Libreria Python Bottle. 
  Fast and simple WSGI-framework for small web-applications.
  bottle.py is a fast and simple micro-framework for python web-applications

import bottle
import os

@bottle.route('/')
def home_page():
	return "Hello World\n"

@bottle.route('/cmd')
def list_Dir():
	nos = os.system('ls -alh')
	return nos

@bottle.route('/hostname')
def host_Name():
	os.system('hostname')
	
bottle.debug(True)
bottle.run(host='localhost', port=8080)



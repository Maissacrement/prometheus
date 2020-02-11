#!make

install:
	pip3 install -r requirements.txt

dev:
	python3 ./wsgi.py

prod-test:
	uwsgi --socket 0.0.0.0:8000 --protocol=http -w wsgi

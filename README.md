![Fxapi](https://i.imgur.com/42kJunI.png)

# FXaPi

FXaPi is a unofficial api module for the site [fxp.co.il](https://www.fxp.co.il)
I wrote it for fun and for my own personal use.

## How it works

The module emulates the browser actions by sending requests to the site server.
The module doesn't load any type of files while sending requests to the site and that makes it faster 

## Installation

This package can be installed from GitHub or with `pip` (install from github for an up to date code)
```
pip install fxapi
```

## Basic Usage
```python
from fxapi import Client

user = Client()

if user.login('amitavr', 'PASSWORD'):
	print(f'Logged in as - {user.username}')

	new_thread = user.create_thread(21, 'Title', 'Content', prefix='dis')
	if new_thread:
		print(f'New thread created successfully - {new_thread}')

		user.post_comment(new_thread, 'First Comment')

```

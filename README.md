# Django Blog

A Django Blogging Application 

---
## Setup Instructions

Install [Python](https://python.org/downloads) (version 3.8 or later)

Install [Git](https://git-scm.com/downloads)

Install [SQLite](https://www.sqlite.org/download.html)

Clone this repo and `cd` into it
```bash
$ git clone https://github.com/blessed-sibanda/django-blog
$ cd django-blog 
```

Install pipenv using pip
```bash
$ pip install --user pipenv
```

Create a pipenv virtual environment
```bash
$ pipenv shell --python 3.8
```

Install pip dependencies
```bash
(django-blog) $ pipenv install
```

Run migrations
```bash
(django-blog) $ python manage.py migrate
```

Run the development server
```bash
(django-blog) $ python manage.py migrate
```

Visit the blog at [http://127.0.0.1:8000/blog](http://127.0.0.1:8000/blog)

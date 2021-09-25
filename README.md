# Django Blog

A Django Blogging Application

---

## Features

- staff users can create posts

- users can share posts via email

- posts can be tagged

- users can perform a full-text search on posts

- users can comment on posts

- inappropriate comments can be disabled via the admin

- users can subscribe to an RSS feed for the posts

- the site has a sitemap

## Setup Instructions

### Install [Git](https://git-scm.com/downloads)

Clone this repo and `cd` into it

```bash
$ git clone https://github.com/blessed-sibanda/django-blog
$ cd django-blog
```

### Install [Python](https://python.org/downloads) (version 3.8 or later)

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

### Install [PostgreSQL](https://www.postgresql.org/download/)

Open postgres terminal and psql

```bash
$ sudo su - postgres
$ psql
```

Create database

```psql
postgres=# CREATE DATABASE blog;
postgres=# CREATE USER blog;
postgres=# GRANT ALL ON DATABASE blog to "blog";
postgres=# ALTER USER blog PASSWORD '1234pass';
postgres=# ALTER USER blog CREATEDB;
postgres=# \q;
```

Exit postgresql shell

```bash
$ exit
```

Run database migrations (in project root folder)

```bash
(django-blog) $ python manage.py migrate
```

Create a superuser account

```bash
(django-blog) $ python manage.py createsuperuser
```

Load sample data using fixtures

```bash
(django-blog) $ python manage.py loaddata blog/fixtures/posts.json
```

Run the development server

```bash
(django-blog) $ python manage.py runserver
```

Login to the blog admin site at [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin) using the superuser account credentials

Add more posts via the admin panel and view the blog home page at [http://127.0.0.1:8000/blog](http://127.0.0.1:8000/blog)

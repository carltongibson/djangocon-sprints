# dcus2019sprints
Notes for "Getting started contributing to Django" sprints workshop.


## Django's contributing guide

The canonical docs here are [the Contributing Guide](https://docs.djangoproject.com/en/dev/internals/contributing/).
The link there is to the index page. There's a lot to it! Explore.

Two good starting points are:

* [Advice for new contributors](https://docs.djangoproject.com/en/dev/internals/contributing/new-contributors/)
* [Writing your first patch for Django](https://docs.djangoproject.com/en/dev/intro/contributing/) (Tutorial)


## Getting set up with the code

The goals is to get Django source code and be able to run the test suite.

1. Fork the main django/django repo on GitHub
2. `git clone` your fork. — You've now got Django's source code on your laptop. 💃
3. Create a virtual environment.
4. Install Django as _editable_: `pip install -e .`
5. Install the test requirements. `cd tests && pip install -r requirements/py3.txt`
6. Run the tests. `./runtests.py`

This should run the tests locally against SQLite. They should pass.

If you have difficulties installing the requirements, there may be missing
dependencies and such. We'll have to look into those. Reach out.


### Using Docker

An alternative is to use Docker. We have a [`django-docker-box`](https://github.com/django/django-docker-box)
project for that.

This option is particularly good if you want to work on the ORM, because it
lets you test against all the supported DBs.

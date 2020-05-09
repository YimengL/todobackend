# Docker in AWS Todobackend Sample Application

This repository provides a sample application based upon the [Todo-backend project](https://www.todobackend.com).

#### Install dependencies
```shell script
$ pipenv shell
(todobackend) $ pipenv install -r src/requirements.txt
```

#### Run Unit Test
```shell script
$ pipenv shell
(todobackend) $ pipenv install -r src/requirements_test.txt
(todobackend) $ cd src
(todobackend) $ python manage.py test --settings todobackend.settings_test
```


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

#### Build Docker Image
```shell script
$ docker build -t todobackend-release .
```

#### Run the server with uwsgi server
```shell script
$ docker run -it --rm -p 8000:8000 todobackend-release uwsgi \
--http=0.0.0.0:8000 --module=todobackend.wsgi --master
```

*****

### Docker Compose

#### Use docker-compose to build and run the test

```shell script
$ docker-compose build test
$ docker-compose run test
```

#### Use docker-compose to run the release
```shell script
$ docker-compose up release # build + run
```



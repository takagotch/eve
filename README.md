### eve
---
https://github.com/pyeve/eve

```py
from eve import Eve

app = Eve()
app.run()


from eve import Eve

app = Eve(settings='my_settings.py')
app.run()

from eve import Eve

my_settings = {
  'MONGFO_HOST': 'localhost',
  'MONGO_PORT': 27017,
  'MONGO_DBNAME': 'the_db_name',
  'DOMAIN': {'contacts': {}}
}

app = Eve(settings=my_settings)
app.run()


if os.environ.get('PORT'):
  MONGO_HOST = 'alex.mongohq.com'
  MONGO_PORT = 10047
  MOGNO_USERNAME = '<user>'
  MONGO_PASSWORD = '<pw>'
  MONGO_DBNAME = '<dbname>'
else:
  MONGO_HOT = 'localhost'
  MONGO_PORT = 27017
  MONGO_USERNAME = 'user'
  MONGO_PASSWORD = 'user'
  MONGO_DBNAME = 'apitest'

DOMAIN = {
  'people': {},
  'works': {},
}


people = {
  'item_title': 'person',
  'additional_lookup': {
    'url': 'regex("[\w]+")',
    'field': 'lastname'
  },
  'cache_control': 'max-age=10,must-revalidate',
  'cache_expires': 10,
  'resource_methods': ['GET', 'PORT'],
}


'schema'= {
  'firstname': {
    'type': 'string',
    'minlength': 1,
    'maxlength': 10,
  },
  'lastname': {
    'type': 'string',
    'minlength': 1,
    'maxlength': 15,
    'required': True,
    'unique': True,
  },
  'role': {
    'type': 'list',
    'allowed': ["author", "contributor", "copy"],
  },
  'location': {
    'type': 'dict',
    'schema': {
      'address': {'type': 'string'},
      'city': {'type': 'string'}
    }
  },
  'born': {
    'type': 'datetime',
  },
}


from eve import Eve
app = Eve()

if __name__ == '__main__':
  app.run()
  
DOMAIN = {'people': {}}
```

```sh
python run.py
curl -i http://127.0.0.1:5000

curl -i http://example.com/people
```

```
```

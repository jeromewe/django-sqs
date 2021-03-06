# django-sqs-mq

# 概括

#### Supported Django and Python versions

Django \ Python | 3.4 | 3.5 | 3.6 | 3.7 | 3.8 |
--------------- | --- | --- | --- | --- | --- |
1.11 |  *  |  *  |  *  |  *  |  *  |
2.0  |  *  |  *  |  *  |  *  |  *  |

## Documentation

### Installation
To install django-sqs-mq:
```shell
$ pip install django-sqs-mq
```


### Usage

Integrating django-sqs-mq support into your app is a three-step process:

1. create your notice types
1. create your notice templates
1. send notifications

#### Creating Notice Types

You need to call `NoticeType` once to
create the notice types for your application in the database.
 
* `label` is the internal shortname that will be used for the type
* `display` is what the user sees as the name of the notification type
* `description` is a short description

For example:

```python
import json
from django_sqs.launcher import SqsLauncher

kwargs = {

}
kwargs.update({'logs_type': 'operate_logs'})

SqsLauncher().send_message(json.dumps(**kwargs, ensure_ascii=False))
```

## Contribute



## Code of Conduct



## License

Copyright (c) 2018-2020   [MIT license](https://opensource.org/licenses/MIT).
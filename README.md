# smshub-org


### Описание на русском ниже

Wrapper for automatic reception of SMS-messages by smshub.org, sms-activate.ru, 5sim and many others.

### Installation
You can install or upgrade package with:
```
$ pip install smshuborg --upgrade
```
Or you can install from source with:
```
$ git clone https://github.com/Derad6709/python-sms
$ cd python-smshub-org
$ python setup.py install
```
...or install from source buth with pip
```
$ pip install git+https://github.com/Derad6709/python-sms
```
### Example
```python
from pythonsms import Sms, SmsService, GetNumber

wrapper = Sms('API KEY')

activation = GetNumber(
	service=SmsService().Youla,
).request(wrapper)

input('Press enter if you sms was sent')

activation.was_sent().request(wrapper)
code = activation.wait_code(wrapper=wrapper)
print(code)
```
More examples located in /example/ dir

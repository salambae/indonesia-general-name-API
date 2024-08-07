# Indonesia Common Names API

### Base URL
```https://salambae.pythonanywhere.com/api/v1/indonesia-general-name```

### Endpoint
```https://salambae.pythonanywhere.com/api/v1/indonesia-general-name [GET]```
The output will be:
```
{
    "data": [
        {
            "firstName": "Ahmad",
            "lastName": "Fauzi"
        },
    ]
}
```

# Example usage
### Here's an example of how to access my API (using Python)
All data from API will be read, no exception
```Python
import requests
base_url = 'https://salambae.pythonanywhere.com/api/v1/indonesia-general-name'
try:
    response = requests.get(base_url)
    response.raise_for_status()
    for i in range(99):
        print(f"{response.json()['data'][i]["firstName"]} {response.json()['data'][i]["lastName"]}")
except requests.exceptions.RequestException as e:
    print(f'Error request{e}'
```

### Accessing the API using command prompt
Also, you can access the API from command prompt for example
```Prompt
curl https://salambae.pythonwhere.com/api/v1/indonesia-general-name
```

### Generating random name
Use ```randint()``` method for generating a random name, example
```Python
import requests
import random
base_url = 'https://salambae.pythonanywhere.com/api/v1/indonesia-general-name'
try:
    response = requests.get(base_url)
    response.raise_for_status()
    i = random.randint(0,99)
    print(f"{response.json()['data'][i]["firstName"]} {response.json()['data'][i]["lastName"]}")
except requests.exceptions.RequestException as e:
    print(f'Error request: {e}')
```

### Swap the firstName with lastname
Like the previous method, you can swap the last name with first name using ```randint()``` for example
```Python
import requests
import random
base_url = 'https://salambae.pythonanywhere.com/api/v1/indonesia-general-name'
try:
    response = requests.get(base_url)
    response.raise_for_status()
    i = random.randint(0,99)
    x = random.randint(0, 99)
    print(f"{response.json()['data'][i]["firstName"]} {response.json()['data'][x]["lastName"]}")
except requests.exceptions.RequestException as e:
    print(f'Errror request: {e}')
```

# Getting Started
API (Aplication Programming Interface) are essential tools for modern software development, enabling seamless communication between different systems and services.

# References
pythonanywhere.com

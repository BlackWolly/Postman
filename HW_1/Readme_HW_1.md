# POSTMAN
## _HOMEWORK 1, GET & POST_

- Protocol: http
- IP: 162.55.220.72
- Port: 5005

##### **REQUEST №1** 
Method: GET
EndPoint: /get_method
request url params: 
 name: Pavlo
 age: 36
##### **RESPONSE №1**
```sh
[
    "Pavlo",
    "36"
]
```

##### **REQUEST №2** 
Method: POST
EndPoint: /user_info_3
request form data: 
 name: Pavlo
 age: 36
 salary: 500
 ##### **RESPONSE №2**
 ```sh
{
    "age": "36",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "u_salary_1_5_year": 2000
    },
    "name": "Pavlo",
    "salary": 500
}
```

##### **REQUEST №3** 
Method: GET
EndPoint: /object_info_1
request url params: 
 name: Pavlo
 age: 36
 weight: 70
##### **RESPONSE №3**
 ```sh
{
    "age": 36,
    "daily_food": 0.84,
    "daily_sleep": 175.0,
    "name": "Pavlo"
}
```

##### **REQUEST №4**
Method: GET
EndPoint: /object_info_2
request url params: 
 name: Pavlo
 age: 36
 salary: 600
##### **RESPONSE №4**
 ```sh
{
    "person": {
        "u_age": 36,
        "u_name": [
            "Pavlo",
            600,
            36
        ],
        "u_salary_5_years": 2520.0
    },
    "qa_salary_after_1.5_year": 1980.0,
    "qa_salary_after_12_months": 1620.0,
    "qa_salary_after_3.5_years": 2280.0,
    "qa_salary_after_6_months": 1200,
    "start_qa_salary": 600
}
```
##### **REQUEST №5**
Method: GET
EndPoint: /object_info_3
request url params: 
 name: Pavlo
 age: 36
 salary: 700
##### **RESPONSE №5**
 ```sh
{
    "age": "36",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "pets": {
            "cat": {
                "age": 3,
                "name": "Sunny"
            },
            "dog": {
                "age": 4,
                "name": "Luky"
            }
        },
        "u_salary_1_5_year": 2800
    },
    "name": "Pavlo",
    "salary": 700
}
```

##### **REQUEST №6**
Method: GET
EndPoint: /object_info_4
request url params: 
 name: Pavlo
 age: 36
 salary: 700
##### **RESPONSE №6**
 ```sh
{
    "age": 36,
    "name": "Pavlo",
    "salary": [
        700,
        "1400",
        "2100"
    ]
}
```

##### **REQUEST №7**
Method: POST
EndPoint: /user_info_2
request form data: 
 name: Pavlo
 age: 36
 salary: 700
 
##### **RESPONSE №7**
 ```sh
{
    "person": {
        "u_age": 36,
        "u_name": [
            "Pavlo",
            700,
            36
        ],
        "u_salary_5_years": 2940.0
    },
    "qa_salary_after_1.5_year": 2310.0,
    "qa_salary_after_12_months": 1890.0000000000002,
    "qa_salary_after_3.5_years": 2660.0,
    "qa_salary_after_6_months": 1400,
    "start_qa_salary": 700
}
```

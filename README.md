
# Rookmotion API v2 (Develop)

Collection of public methods for the RookMotion API.

## Indices

* [Centers](#centers)

  * [Branch](#1-branch)
  * [Chain](#2-chain)
  * [Room](#3-room)
  * [retrive center](#4-retrive-center)
  * [show center](#5-show-center)

* [Rewards](#rewards)

  * [Retrive rewards user](#1-retrive-rewards-user)

* [Sensors](#sensors)

  * [Add sensor to user](#1-add-sensor-to-user)
  * [Remove sensor from user](#2-remove-sensor-from-user)
  * [Retrive sensors from user](#3-retrive-sensors-from-user)
  * [Update sensor](#4-update-sensor)
  * [retrive sensors level](#5-retrive-sensors-level)

* [Server](#server)

  * [Retrive server datetime](#1-retrive-server-datetime)

* [Summaries](#summaries)

  * [Retrive summaries types](#1-retrive-summaries-types)

* [Training type](#training-type)

  * [Retrive training types](#1-retrive-training-types)

* [Trainings](#trainings)

  * [Add training to user](#1-add-training-to-user)
  * [Remove training user](#2-remove-training-user)
  * [Retrieve training information of user](#3-retrieve-training-information-of-user)
  * [Retrive all trainings](#4-retrive-all-trainings)
  * [Retrive sum summaries](#5-retrive-sum-summaries)
  * [Retrive trainings of user](#6-retrive-trainings-of-user)

* [Users](#users)

  * [Add user to RookMotion](#1-add-user-to-rookmotion)
  * [External user](#2-external-user)
  * [Information](#3-information)
  * [Remove user for RookMotion](#4-remove-user-for-rookmotion)
  * [Remove user for nivel](#5-remove-user-for-nivel)
  * [Retrieve user status](#6-retrieve-user-status)
  * [Retrive client users](#7-retrive-client-users)
  * [physiological variables](#8-physiological-variables)
  * [update user email](#9-update-user-email)


--------


## Centers



### 1. Branch



***Endpoint:***

```bash
Method: 
Type: 
URL: 
```



### 2. Chain



***Endpoint:***

```bash
Method: 
Type: 
URL: 
```



### 3. Room



***Endpoint:***

```bash
Method: 
Type: 
URL: 
```



### 4. retrive center



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/centers/search
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept-Language | en |  |
| token-user | {{token_user}} |  |
| Accept | application/json |  |



***More example Requests/Responses:***


##### I. Example Request: retrive center


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept-Language | en |  |
| token-user | {{token_user}} |  |
| Accept | application/json |  |



##### I. Example Response: retrive center
```js
{
    "data": [
        {
            "chain_uuid": "{{chain_uuid}}",
            "chain_name": "rookmotion uno",
            "branch_uuid": "{{branch_uuid}}",
            "branch_name": "centro de prueba",
            "branch_description": "prueba de centro",
            "lang_types": 1,
            "measurement_system": "metric_system",
            "location": {
                "uuid": "{{location_uuid}}",
                "address_line_1": "ignacio allende 21, amp torre blanca",
                "address_line_2": null,
                "address_line_3": null,
                "country": "méxico",
                "state": "ciudad de méxico",
                "city": "miguel hidalgo",
                "zip_code": "11289",
                "location_point": "19.453903328596336, -99.20001526137233"
            },
            "multimedia": [
                {
                    "uuid": "{{multimedia_uuid}}",
                    "name": "eyU69phf1tXKpXAbJZnd2MQ1p5OGRy5QDjtlDeKJ.jpg",
                    "url": "https://api-media-root.s3.us-east-2.amazonaws.com/images_branch/eyU69phf1tXKpXAbJZnd2MQ1p5OGRy5QDjtlDeKJ.jpg",
                    "media_type": "image",
                    "usage_type": "gallery"
                }
            ],
            "rooms": [
                {
                    "uuid": "{{room_uuid}}",
                    "name": "agregando remot",
                    "logo_image": null,
                    "background_image": null
                }
            ]
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/centers/search?page=1",
        "last": "http://apiv2.test/api/v2/centers/search?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/centers/search?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/centers/search",
        "per_page": 250,
        "to": 2,
        "total": 2
    }
}
```


***Status Code:*** 200

<br>



### 5. show center



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/centers/{{branch_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept-Language | en |  |
| Accept | application/json |  |
| token-admin | {{token_admin}} |  |



***More example Requests/Responses:***


##### I. Example Request: show center


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept-Language | en |  |
| Accept | application/json |  |
| token-admin | {{token_admin}} |  |



##### I. Example Response: show center
```js
{
    "chain_uuid": "{{chain_uuid}}",
    "chain_name": "rookmotion uno",
    "branch_uuid": "{{branch_uuid}}",
    "branch_name": "centro de prueba",
    "branch_description": "prueba de centro",
    "lang_types": 1,
    "measurement_system": "metric_system",
    "location": {
        "uuid": "{{location_uuid}}",
        "address_line_1": "ignacio allende 21, amp torre blanca",
        "address_line_2": null,
        "address_line_3": null,
        "country": "méxico",
        "state": "ciudad de méxico",
        "city": "miguel hidalgo",
        "zip_code": "11289",
        "location_point": "19.453903328596336, -99.20001526137233"
    },
    "multimedia": [
        {
            "uuid": "multimedia_uuid",
            "name": "eyU69phf1tXKpXAbJZnd2MQ1p5OGRy5QDjtlDeKJ.jpg",
            "url": "https://api-media-root.s3.us-east-2.amazonaws.com/images_branch/eyU69phf1tXKpXAbJZnd2MQ1p5OGRy5QDjtlDeKJ.jpg",
            "media_type": "image",
            "usage_type": "gallery"
        }
    ],
    "rooms": [
        {
            "uuid": "{{room_uuid}}",
            "name": "agregando remot",
            "logo_image": null,
            "background_image": null
        }
    ]
}
```


***Status Code:*** 200

<br>



## Rewards



### 1. Retrive rewards user



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/rewards/user/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive rewards user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrive rewards user
```js
{
    "data": [
        {
            "training_uuid": "25c1af02-84db-41a1-875f-3809144fdfcc",
            "calories_points": "0.0000"
        },
        {
            "training_uuid": "9be71509-6e57-4788-b5b6-98062749a6aa",
            "calories_points": "2.0000"
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/rewards/user/{{user_uuid}}?page=1",
        "last": "http://apiv2.test/api/v2/rewards/user/{{user_uuid}}?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/rewards/user/{{user_uuid}}?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/rewards/user/{{user_uuid}}",
        "per_page": 250,
        "to": 8,
        "total": 8
    }
}
```


***Status Code:*** 200

<br>



## Sensors
In this section you will find a list of the resources available in the RookMotion API to manage user sensors.



### 1. Add sensor to user



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://api2.rookmotion.rookeries.dev/api/v2/sensors/user/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Body:***

```js        
{
    "name": "HW702T-0529625",
    "ownership_type": "owned"
}
```



***More example Requests/Responses:***


##### I. Example Request: Add sensor to user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Body:***

```js        
{
    "name": "RM29T-077911",
    "mac": "7A:4B:B8:A2:BC:8B",
    "ownership_type": "owned"
}
```



##### I. Example Response: Add sensor to user
```js
{
    "result": "added",
    "sensor_uuid": "{{sensor_uuid}}"
}
```


***Status Code:*** 201

<br>



### 2. Remove sensor from user



***Endpoint:***

```bash
Method: DELETE
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/sensors/7d977897-4bee-48b4-bde2-e8e6385a0443/user/4ae34029-b578-4939-a5e1-f762d2291a3b
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | {{token_user}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Remove sensor from user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Status Code:*** 204

<br>



### 3. Retrive sensors from user



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/sensors/user/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive sensors from user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrive sensors from user
```js
{
    "data": [
        {
            "sensor_uuid": "{{sensor_uuid}}",
            "sensor_name": "RM29T-077911",
            "sensor_mac": "7A:4B:B8:A2:BC:8B",
            "ownership_type": "owned",
            "updated_at": "2021-03-31 14:49:33"
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/sensors/user/{{user_uuid}}?page=1",
        "last": "http://apiv2.test/api/v2/sensors/user/{{user_uuid}}?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/sensors/user/{{user_uuid}}?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/sensors/user/{{user_uuid}}",
        "per_page": 30,
        "to": 1,
        "total": 1
    }
}
```


***Status Code:*** 200

<br>



### 4. Update sensor



***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: https://api2.rookmotion.rookeries.dev/api/v2/sensors/{{sensor_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Body:***

```js        
{
    "name": "RM29A-T9291A",
    "mac": "7C:4C:BA:A2:B4:8D",
    "mac_type": "public"
}
```



***More example Requests/Responses:***


##### I. Example Request: Update sensor


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Body:***

```js        
{
    "name": "RM48T-476377",
    "mac": "77:4C:B2:F8:BE:8E",
    "mac_type": "public"
}
```



##### I. Example Response: Update sensor
```js
{
    "result": "updated"
}
```


***Status Code:*** 200

<br>



### 5. retrive sensors level



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/sensors
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: retrive sensors level


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-admin | {{token_auth}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: retrive sensors level
```js
{
    "data": [
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "HW702A-0582625",
            "sensor_mac": null,
            "updated_at": "2019-09-04 11:48:27"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "TK77A-T9291B",
            "sensor_mac": "f4-8e-38-f5-49-c1",
            "sensor_id_center": "1",
            "updated_at": "2021-11-29 18:24:28"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "HW702A-0582625",
            "sensor_mac": null,
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "Polar-H7-90FAFE10",
            "sensor_mac": "",
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "RookC2-0057861",
            "sensor_mac": "EB:C4:A2:BB:1D:A7",
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "Rook-i-0162598",
            "sensor_mac": "F7:65:BF:4F:C8:15",
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "Rook-i-0196532",
            "sensor_mac": "C3:D3:AF:7A:34:B8",
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "Rook-i-0162618",
            "sensor_mac": "CA:53:81:8E:48:A8",
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "Rook-i-0196143",
            "sensor_mac": "F1:98:41:BC:1B:A6",
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        },
        {
            "sensor_uuid": "{{ sensor_uuid }}",
            "sensor_name": "RM29A-T9291A",
            "sensor_mac": "7C:4C:BA:A2:B4:8D",
            "ownership_type": "owned",
            "user_uuid": "{{ user_uuid }}",
            "user_email": "{{ user_email }}",
            "updated_at": "2021-11-16 12:14:38"
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/sensors?page=1",
        "last": "http://apiv2.test/api/v2/sensors?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/sensors?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/sensors",
        "per_page": 250,
        "to": 10,
        "total": 10
    }
}
```


***Status Code:*** 200

<br>



## Server
In this section, you will find an end point to get the server date.



### 1. Retrive server datetime



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/server/datetime
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive server datetime


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Accept-Language | en |  |



##### I. Example Response: Retrive server datetime
```js
{
    "datetime": "2021-03-31 14:38:47"
}
```


***Status Code:*** 200

<br>



## Summaries
In this section, you will find a list of the resources available in the RookMotion API to obtain the Summaries



### 1. Retrive summaries types



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/summaries
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive summaries types


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrive summaries types
```js
{
    "data": [
        {
            "id": 1,
            "summary_type_uuid": "537683b5-4edd-4981-b301-47c472beb532",
            "summary_name": "duration_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 2,
            "summary_type_uuid": "5ea15fce-6756-42ef-931d-18173a67b9c1",
            "summary_name": "z0_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 3,
            "summary_type_uuid": "718e51fd-7507-4c27-b1c7-233776a29c9b",
            "summary_name": "z1_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 4,
            "summary_type_uuid": "d225c105-5ce7-47dc-ac0f-a1b2746dfbb9",
            "summary_name": "z2_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 5,
            "summary_type_uuid": "b40bc80e-f50f-47c6-b244-149b4e1022e9",
            "summary_name": "z3_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 6,
            "summary_type_uuid": "3dc3aad7-501e-4cb1-ac13-096db3071780",
            "summary_name": "z4_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 7,
            "summary_type_uuid": "47e5ac87-f335-4391-96cc-388fe7da3d17",
            "summary_name": "z5_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 8,
            "summary_type_uuid": "5855d7bd-ee5d-4f7b-b8fe-b130f94e6a7f",
            "summary_name": "z6_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 9,
            "summary_type_uuid": "d079f9e6-e204-4a55-b30c-94b1cec3d23b",
            "summary_name": "z7_time_tot",
            "group": "time",
            "units": "s"
        },
        {
            "id": 100,
            "summary_type_uuid": "bb9d2ae9-79b8-4ad6-8256-dd45310687a3",
            "summary_name": "heart_rate_min",
            "group": "heart_rate",
            "units": "bpm"
        },
        {
            "id": 101,
            "summary_type_uuid": "5b1960b9-c490-496e-a20a-cd58d050eb95",
            "summary_name": "heart_rate_avg",
            "group": "heart_rate",
            "units": "bpm"
        },
        {
            "id": 102,
            "summary_type_uuid": "99ce771b-9fc0-4d5a-bbc4-76a625578bd9",
            "summary_name": "heart_rate_max",
            "group": "heart_rate",
            "units": "bpm"
        },
        {
            "id": 200,
            "summary_type_uuid": "d8966576-9b04-4504-a96e-daf6b30813c2",
            "summary_name": "heart_rate_variability_min",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 201,
            "summary_type_uuid": "ffedada6-9e38-41d1-80bd-58f5fe00f316",
            "summary_name": "heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 202,
            "summary_type_uuid": "c9b828d5-b34b-4285-9237-4e07bdce507f",
            "summary_name": "heart_rate_variability_max",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 203,
            "summary_type_uuid": "5344d0dc-d640-400c-91f4-63f4781f4672",
            "summary_name": "z0_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 204,
            "summary_type_uuid": "0e5159df-5c18-487d-b912-5d5da93aafe8",
            "summary_name": "z1_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 205,
            "summary_type_uuid": "c7c5eec2-f0a4-48f5-93c2-a77645aa863a",
            "summary_name": "z2_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 206,
            "summary_type_uuid": "129cab69-3a34-4b15-8597-0958a708f6ac",
            "summary_name": "z3_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 207,
            "summary_type_uuid": "9a5d3273-3188-47a6-96ef-9b080463c22b",
            "summary_name": "z4_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 208,
            "summary_type_uuid": "19a3dc12-ace3-4520-9f45-fd0258bf7ba6",
            "summary_name": "z5_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 209,
            "summary_type_uuid": "6006596c-5ad6-4355-83e2-894bc536fbc6",
            "summary_name": "z6_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 210,
            "summary_type_uuid": "15561cdc-3421-4f7c-8251-009e7ab44c86",
            "summary_name": "z7_heart_rate_variability_avg",
            "group": "heart_rate_variability",
            "units": "ms"
        },
        {
            "id": 300,
            "summary_type_uuid": "ee1e726d-84ca-4440-872f-3ae89896a800",
            "summary_name": "effort_min",
            "group": "effort",
            "units": "percentage"
        },
        {
            "id": 301,
            "summary_type_uuid": "f462f15e-dc65-477b-b223-1b2ebcace0e0",
            "summary_name": "effort_avg",
            "group": "effort",
            "units": "percentage"
        },
        {
            "id": 302,
            "summary_type_uuid": "8e06c211-f276-4ab4-a9aa-508c387cbd7c",
            "summary_name": "effort_max",
            "group": "effort",
            "units": "percentage"
        },
        {
            "id": 400,
            "summary_type_uuid": "6ce6a4a1-fef7-423a-b9bf-e23de03fd006",
            "summary_name": "calories_tot",
            "group": "calories",
            "units": "kcal"
        },
        {
            "id": 401,
            "summary_type_uuid": "5282bc3b-c7ad-447a-bc43-48cea101bc41",
            "summary_name": "z0_calories_tot",
            "group": "calories",
            "units": "kcal"
        },
        {
            "id": 402,
            "summary_type_uuid": "cde95f55-2546-41a3-8329-b97d6bd20c96",
            "summary_name": "z1_calories_tot",
            "group": "calories",
            "units": "kcal"
        },
        {
            "id": 403,
            "summary_type_uuid": "e2fc989e-e856-4b85-a27b-9dced7421824",
            "summary_name": "z2_calories_tot",
            "group": "calories",
            "units": "kcal"
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/summaries?page=1",
        "last": "http://apiv2.test/api/v2/summaries?page=3",
        "prev": null,
        "next": "http://apiv2.test/api/v2/summaries?page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 3,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/summaries?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": "http://apiv2.test/api/v2/summaries?page=2",
                "label": "2",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/summaries?page=3",
                "label": "3",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/summaries?page=2",
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/summaries",
        "per_page": 30,
        "to": 30,
        "total": 75
    }
}
```


***Status Code:*** 200

<br>



## Training type
In this section, you will find a list of the resources available in the RookMotion API to obtain the Type Training



### 1. Retrive training types



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/trainings/type
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive training types


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept-Language | en |  |



##### I. Example Response: Retrive training types
```js
{
    "data": [
        {
            "training_type_uuid": "1dc7e4e1-8c85-4f06-8bcd-cccbf53ad069",
            "trainig_name": "soccer",
            "use_heart_rate": 1
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/trainings/type?page=1",
        "last": "http://apiv2.test/api/v2/trainings/type?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/trainings/type?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/trainings/type",
        "per_page": 30,
        "to": 1,
        "total": 1
    }
}
```


***Status Code:*** 200

<br>



## Trainings
In this section you will find a list of the resources available in the RookMotion API to manage user trainings.



### 1. Add training to user



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://api2.rookmotion.rookeries.dev/api/v2/trainings/user/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | {{token_user}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |
| key-device | e47fe55db83dcb41 |  |
| product | android |  |
| model | Android API 30 |  |
| version | 1.0 |  |



***Body:***

```js        
{
    "start":"2021-12-08 09:46:58",
    "end":"2021-12-08 09:48:57",
    "training_type_uuid": "{{training_type_uuid}}",
    "sensor_uuid":"{{sensor_uuid}}",
    "device_type":"remote",
    "groupal_mode": 0,
    "room_uuid": "{{room_uuid}}",
    "records": {
        "hr_derived_records":[
            {
                "timestamp": "2020-10-20 20:20:20",
                "heart_rate": 80,
                "effort": 100,
                "calories": 2000,
                "heart_rate_variability": 2000
            }, 
            {
                "timestamp": "2020-10-20 20:20:21",
                "heart_rate": 81,
                "effort": 99,
                "calories": 2001,
                "heart_rate_variability": 2000
            } 
        ],
        "steps_derived_records":[
            {
                "timestamp": "2020-10-20 20:20:20",
                "steps": 5000,
                "cadence": 20
            }, 
            {
                "timestamp": "2020-10-20 20:20:21",
                "steps": 5001,
                "cadence": 21
            }
        ]
    },
    "summaries": [
        {
            "summary_type_id": 2,
            "value": 3600
        },
        {
            "summary_type_id": 400,
            "value": 500
        }
    ]
}
```



***More example Requests/Responses:***


##### I. Example Request: Add training to user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | {{token_user}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |
| key-device | e47fe55db83dcb41 |  |
| product | android |  |
| model | Android API 30 |  |
| version | 1.0 |  |



***Body:***

```js        
{
    "start":"2021-12-08 09:46:58",
    "end":"2021-12-08 09:48:57",
    "training_type_uuid": "{{training_type_uuid}}",
    "sensor_uuid":"{{sensor_uuid}}",
    "device_type":"remote",
    "groupal_mode": 0,
    "room_uuid": "{{room_uuid}}",
    "records": {
        "hr_derived_records":[
            {
                "timestamp": "2020-10-20 20:20:20",
                "heart_rate": 80,
                "effort": 100,
                "calories": 2000,
                "heart_rate_variability": 2000
            }, 
            {
                "timestamp": "2020-10-20 20:20:21",
                "heart_rate": 81,
                "effort": 99,
                "calories": 2001,
                "heart_rate_variability": 2000
            } 
        ],
        "steps_derived_records":[
            {
                "timestamp": "2020-10-20 20:20:20",
                "steps": 5000,
                "cadence": 20
            }, 
            {
                "timestamp": "2020-10-20 20:20:21",
                "steps": 5001,
                "cadence": 21
            }
        ]
    },
    "summaries": [
        {
            "summary_type_id": 2,
            "value": 3600
        },
        {
            "summary_type_id": 400,
            "value": 500
        }
    ]
}
```



##### I. Example Response: Add training to user
```js
{
    "result": "added",
    "training_uuid": "f930a589-5e0e-4ec9-9b2c-fbececf70323"
}
```


***Status Code:*** 201

<br>



### 2. Remove training user



***Endpoint:***

```bash
Method: DELETE
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/trainings/0c0ece0e-8e56-44bd-920c-4f50fabdf355
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | eyJpdiI6IldDSVV1eXZQTnVrRVd4Qmh0ek9sOFE9PSIsInZhbHVlIjoiN0FadzZ0Y0xUVnh2ZWJWWFNMU25PVTQzYmhwNmViNzBuWXJrSVovV1JJd3VUZFZBcEw0RnpnMmJKTlRqZXROYSIsIm1hYyI6ImNkYmZmMDZmYjlhNjhkNzUzYTE3NzMzYzRjZjM4MTU2OTlhMTc5OWMxYzVkY2E2M2RlYTE1YTI1ZjBhY2VhMzUiLCJ0YWciOiIifQ== |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Remove training user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Status Code:*** 204

<br>



### 3. Retrieve training information of user



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/trainings/f930a589-5e0e-4ec9-9b2c-fbececf70323/show
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | eyJpdiI6ImtQQlNNVndIdk92SVBwNlNTN25LSmc9PSIsInZhbHVlIjoiL3h2cUlzbFJxVEYvTGsyMnFKYUN1dnZBVmxJQ1JPZTlGUW9idkQ1UWtjQU9KL1dHN0s4UnY4Mk93YzE4enp6ayIsIm1hYyI6ImQ4ZjE4ZTUzNzkyOTdkNjNiNzkzZDA3ODQ4MTYzNDMyNjAxNzM0MDM4MmMyYWY0NjNjOWRjZWNhYTg2YjE5ZjciLCJ0YWciOiIifQ== |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrieve training information of user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | {{token_user}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrieve training information of user
```js
{
    "start": "2021-12-08 09:46:58",
    "end": "2021-12-08 09:48:57",
    "device_type": "remote",
    "groupal_mode": 0,
    "training_type": {
        "training_name": "jumps",
        "step_options": "jumps",
        "use_steps": 1,
        "use_heart_rate": 1,
        "use_gps": 1,
        "use_cycling": 0
    },
    "sensor": "RM29A-T9291A",
    "origin": {
        "client_room": "agregando remot",
        "client_branch": "centro de prueba",
        "client_center": "rookmotion uno"
    },
    "records": {
        "hr_derived_records": [
            {
                "heart_rate": "80.0000",
                "effort": "100.0000",
                "calories": "2000.0000",
                "heart_rate_variability": "2000.0000",
                "timestamp": "2020-10-20 20:20:20"
            },
            {
                "heart_rate": "81.0000",
                "effort": "99.0000",
                "calories": "2001.0000",
                "heart_rate_variability": "2000.0000",
                "timestamp": "2020-10-20 20:20:21"
            }
        ],
        "steps_derived_records": [
            {
                "steps": "5000.0000",
                "cadence": "20.0000",
                "timestamp": "2020-10-20 20:20:20"
            },
            {
                "steps": "5001.0000",
                "cadence": "21.0000",
                "timestamp": "2020-10-20 20:20:21"
            }
        ]
    },
    "summaries": {
        "z0_time_tot": "3600.0000",
        "calories_tot": "500.0000"
    },
    "rewards": {
        "calories_points": "0.0000"
    }
}
```


***Status Code:*** 200

<br>



### 4. Retrive all trainings



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/trainings/level
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-admin | {{token_admin}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive all trainings


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-admin | {{token_admin}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Query:***

| Key | Value | Description |
| --- | ------|-------------|
| search | sss | Optional, data for search |



##### I. Example Response: Retrive all trainings
```js
{
    "data": [
        {
            "user_name": "prueba",
            "last_name_1": "paterno",
            "last_name_2": "materno",
            "email": "{{ user_email }}",
            "training_uuid": "f930a589-5e0e-4ec9-9b2c-fbececf70323",
            "start": "2021-12-08 09:46:58",
            "device_type": "remote",
            "sensor_name": "RM29A-T9291A",
            "training_name": "jumps"
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/trainings/level?page=1",
        "last": "http://apiv2.test/api/v2/trainings/level?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/trainings/level?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/trainings/level",
        "per_page": 250,
        "to": 8,
        "total": 8
    }
}
```


***Status Code:*** 200

<br>



### 5. Retrive user summaries



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/summaries/2/user/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | {{token_user}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive sum summaries


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrive sum summaries
```js
{
    "result": 0
}
```


***Status Code:*** 200

<br>



### 6. Retrive trainings of user



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/trainings/user/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | eyJpdiI6ImFUc0tyWXVpYVZvWElZSnBOMmcxTGc9PSIsInZhbHVlIjoiMXdSczFkOTQ2SEhHa1ltaEN6QmI1UFhjTlY3TzVKQm9MdTZWS1M1eEFydzlpeFpJTXpTbzBuRC9UeHBDM2NjbiIsIm1hYyI6ImEzYWU3YjA1NjAxYWZjNmQyZTA3YWM2NGRiZjhiYjUzZDJkNTAwZDNhMDllNjUxNTQwOTYxMmVkN2U2Mjk4ZDUiLCJ0YWciOiIifQ== |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive trainings of user


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrive trainings of user
```js
{
    "data": [
        {
            "training_uuid": "bf94fe9c-d96f-4864-8a7f-13faaedac9ac",
            "start": "2021-02-21 10:38:58",
            "end": "2021-02-21 10:40:57",
            "training_type": "soccer",
            "device_type": "app",
            "groupal_mode": 0,
            "processed": 1,
            "summaries": {
                "z0_time_tot": "3600.0000"
            },
            "rewards": {
                "calories_points": "0.0000"
            }
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/trainings/user/{{user_uuid}}?page=1",
        "last": "http://apiv2.test/api/v2/trainings/user/{{user_uuid}}?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/trainings/user/{{user_uuid}}?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/trainings/user/{{user_uuid}}",
        "per_page": 30,
        "to": 1,
        "total": 1
    }
}
```


***Status Code:*** 200

<br>



## Users
In this section you will find a list of the resources available in the RookMotion API to manage users.



### 1. Add user to RookMotion



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://api2.rookmotion.rookeries.dev/api/v2/users
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept-Language | en |  |
| Accept | application/json |  |



***Body:***

```js        
{
    "email": "{{user_email}}"
}
```



***More example Requests/Responses:***


##### I. Example Request: Add user to RookMotion


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept-Language | en |  |
| Accept | application/json |  |



***Body:***

```js        
{
    "email": "{{user_email}}"
}
```



##### I. Example Response: Add user to RookMotion
```js
{
    "user_uuid": "{{user_uuid}}"
}
```


***Status Code:*** 201

<br>



### 2. External user



***Endpoint:***

```bash
Method: 
Type: 
URL: 
```



### 3. Information



***Endpoint:***

```bash
Method: 
Type: 
URL: 
```



### 4. Remove user for RookMotion



***Endpoint:***

```bash
Method: DELETE
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/users/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Remove user for RookMotion


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Status Code:*** 204

<br>



### 5. Remove user for nivel



***Endpoint:***

```bash
Method: DELETE
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/users/{{user_uuid}}/remove
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-admin | {{token_admin}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Remove user for RookMotion


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Status Code:*** 204

<br>



### 6. Retrieve user status



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/users/{{user_email}}/status
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***More example Requests/Responses:***


##### I. Example Request: Retrieve user uuid


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrieve user uuid
```js
{
    "user_uuid": "{{user_uuid}}",
    "user_status": 1,
    "profile_filled_at": "2021-11-09 14:55:22"
}
```


***Status Code:*** 200

<br>



### 7. Retrive client users



***Endpoint:***

```bash
Method: GET
Type: 
URL: https://api2.rookmotion.rookeries.dev/api/v2/users
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |
| token-admin | {{user_token}} |  |



***More example Requests/Responses:***


##### I. Example Request: Retrive client users


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



##### I. Example Response: Retrive client users
```js
{
    "data": [
        {
            "user_uuid": "{{user_uuid}}",
            "name": "prueba",
            "last_name_1": "paterno",
            "last_name_2": "materno",
            "email": "{{user_email}}",
            "pseudonym": "psudo",
            "birthday": "1991-07-29",
            "sex": "male",
            "updated_at": "2021-12-20 12:54:06",
            "url_image": null
        }
    ],
    "links": {
        "first": "http://apiv2.test/api/v2/users?page=1",
        "last": "http://apiv2.test/api/v2/users?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://apiv2.test/api/v2/users?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://apiv2.test/api/v2/users",
        "per_page": 30,
        "to": 1,
        "total": 1
    }
}
```


***Status Code:*** 200

<br>



### 8. physiological variables



***Endpoint:***

```bash
Method: 
Type: 
URL: 
```



### 9. update user email



***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: https://api2.rookmotion.rookeries.dev/api/v2/users/{{user_uuid}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| token-user | {{token_admin}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Body:***

```js        
{
    "email": "{{user_email}}"
}
```



***More example Requests/Responses:***


##### I. Example Request: update user email


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| token-level | {{token_level}} |  |
| Accept | application/json |  |
| Accept-Language | en |  |



***Body:***

```js        
{
    "email": "{{user_email}}"
}
```



##### I. Example Response: update user email
```js
{
    "result": "updated"
}
```


***Status Code:*** 200

<br>



***Available Variables:***

| Key | Value | Type |
| --- | ------|-------------|
| token_rm | client token |  |
| base_url | https://api2.rookmotion.rookeries.dev |  |



---
[Back to top](#rookmotion-api-v2-(develop))
> Made with &#9829; by [thedevsaddam](https://github.com/thedevsaddam) | Generated at: 2021-12-20 15:07:08 by [docgen](https://github.com/thedevsaddam/docgen)

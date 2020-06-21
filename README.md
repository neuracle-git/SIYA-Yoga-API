# SIYA-Yoga-API
API's to Detect and Correct yoga posture from image.

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

[![Generic badge](https://img.shields.io/badge/Version-1.0-COLOR.svg)](https://shields.io/)

## NOTE:
Currently v_1.0 only support 5 Yoga poses i.e:

- halasana left
- halasana right
- trikonasana left
- trikonasana right
- padmasana


### Features

- Detect Yoga Posture.
- Correct Yoga posture.
- Accuracy Score of Yoga.
- Correction key Points of body parts.

# API Usage

## 1. Generate Token API
This api help us to auth all other api's.
- Url
  http://192.241.158.65/api/yoga/v1/generatetoken/
 
- Method
  POST
- Data Params
  key = email
  value = "email id"
  
- Success Response
  - Code: 200
  ```
  {
    "Result": "Token sent in email"
  }
  ```
- Error Response:
  - Code:406
  ```
  {
    {
    "error": [
        "Enter a valid email address."
    ]
  }
    }
  ```
- Sample Call:

## 2. Detect Yoga
This api detect yoga name form yoga posture image.
- Url
  http://192.241.158.65/api/yoga/v1/pose_detection/
 
- Method
  POST
  
<details><summary>Request Data Param</summary>
<p>
  
 ```
  key = email
  value = "email id"
  
  key = "image"
  value = multipart imaege body
 ```
 
</p>
</details>

<details><summary>Header Param</summary>
<p>
  
 ```
 key = "Token"
 value = "token that genertae from genetare token api"
 
 ```
 
</p>
</details>
 
<details><summary>Success Response</summary>
<p>
 
- Code: 200
  ```
  {
    "result": "success",
    "name": "Trikonasana"
  }
  ```
 
 </p>
</details>

<details><summary>Error Response</summary>
<p>
 
 - Code:406
  ```
  {
    {
    "error": [
        "Enter a valid email address."
    ]
  }
    }
  ```
 
 </p>
</details>

## 2. Correct Yoga

This api detect yoga name form yoga posture image.
- Url
  http://192.241.158.65/api/yoga/v1/pose_correction/
 
- Method
  POST
  
<details><summary>Request Data Param</summary>
<p>
  
 ```
  key = email
  value = "email id"
  
  key = "image"
  value = multipart imaege body
 ```
 
</p>
</details>

<details><summary>Header Param</summary>
<p>
  
 ```
 key = "Token"
 value = "token that genertae from genetare token api"
 
 ```
 
</p>
</details>
 
<details><summary>Success Response</summary>
<p>
 
- Code: 200
  ```
  {
    "Result": {
        "id": 4,
        "key_points": [
            {
                "Point": 0,
                "x": 443.4782608695652,
                "y": 556.5217391304348
            },
            {
                "Point": 1,
                "x": 573.9130434782609,
                "y": 521.7391304347826
            },
            {
                "Point": 2,
                "x": 495.6521739130435,
                "y": 260.8695652173913
            },
            {
                "Point": 3,
                "x": 626.0869565217391,
                "y": 591.304347826087
            },
            {
                "Point": 4,
                "x": 417.39130434782606,
                "y": 365.2173913043478
            },
            {
                "Point": 5,
                "x": 573.9130434782609,
                "y": 591.304347826087
            },
            {
                "Point": 6,
                "x": 573.9130434782609,
                "y": 626.0869565217391
            },
            {
                "Point": 7,
                "x": 573.9130434782609,
                "y": 608.695652173913
            },
            {
                "Point": 8,
                "x": 626.0869565217391,
                "y": 434.7826086956522
            },
            {
                "Point": 9,
                "x": 469.5652173913044,
                "y": 556.5217391304348
            },
            {
                "Point": 10,
                "x": 521.7391304347826,
                "y": 434.7826086956522
            },
            {
                "Point": 11,
                "x": 626.0869565217391,
                "y": 452.17391304347825
            },
            {
                "Point": 12,
                "x": 443.4782608695652,
                "y": 556.5217391304348
            },
            {
                "Point": 13,
                "x": 521.7391304347826,
                "y": 434.7826086956522
            },
            {
                "Point": 14,
                "x": 573.9130434782609,
                "y": 521.7391304347826
            }
        ],
        "pair_angles": [
            {
                "pair": [
                    0,
                    1
                ],
                "angle": 14.931417178137533
            },
            {
                "pair": [
                    1,
                    2
                ],
                "angle": 106.69924423399361
            },
            {
                "pair": [
                    2,
                    3
                ],
                "angle": 68.45902408146156
            },
            {
                "pair": [
                    3,
                    4
                ],
                "angle": 132.70938995736148
            },
            {
                "pair": [
                    1,
                    5
                ],
                "angle": 90.0
            },
            {
                "pair": [
                    5,
                    6
                ],
                "angle": 90.0
            },
            {
                "pair": [
                    6,
                    7
                ],
                "angle": 90.0
            },
            {
                "pair": [
                    1,
                    14
                ],
                "angle": 0.0
            },
            {
                "pair": [
                    14,
                    8
                ],
                "angle": 59.03624346792648
            },
            {
                "pair": [
                    8,
                    9
                ],
                "angle": 142.12501634890182
            },
            {
                "pair": [
                    9,
                    10
                ],
                "angle": 66.80140948635182
            },
            {
                "pair": [
                    14,
                    11
                ],
                "angle": 53.130102354155994
            },
            {
                "pair": [
                    11,
                    12
                ],
                "angle": 150.2551187030578
            },
            {
                "pair": [
                    12,
                    13
                ],
                "angle": 57.26477372789238
            }
        ],
        "suggestions_points": [
            [
                0,
                1
            ],
            [
                1,
                2
            ],
            [
                2,
                3
            ],
            [
                1,
                5
            ],
            [
                6,
                7
            ],
            [
                1,
                14
            ],
            [
                14,
                8
            ],
            [
                9,
                10
            ],
            [
                11,
                12
            ],
            [
                12,
                13
            ]
        ],
        "suggestions_names": [
            [
                "Head",
                "Neck"
            ],
            [
                "Neck",
                "Right Shoulder"
            ],
            [
                "Right Shoulder",
                "Right Elbow"
            ],
            [
                "Neck",
                "Left Shoulder"
            ],
            [
                "Left Elbow",
                "Left Wrist"
            ],
            [
                "Neck",
                "Chest"
            ],
            [
                "Chest",
                "Right Hip"
            ],
            [
                "Right Knee",
                "Right Ankle"
            ],
            [
                "Left Hip",
                "Left Knee"
            ],
            [
                "Left Knee",
                "Left Ankle"
            ]
        ],
        "accuracy_score": 40.0
    }
   }

  ```
 </p>
</details>

<details><summary>Error Response</summary>
<p>
 
 - Code:406
  ```
  {
    "error": "Please provide image file"
  }
  ```
</p>
</details>

# Contributing
1. Send us some new yoga poses data on Contact@neuracle.in with your details.
2. suggest some best use cases for that api's and join our Team.

# Our App Link:
[Check out the App](https://play.google.com/store/apps/details?id=in.neuracle.aligny)


# Lens Developer Docs

**INSTALLATION**

**Python Version**

We recommend using python 3.7.

**What is an SDK?**

[SDK](https://clevertap.com/glossary/sdk/) stands for software development kit or devkit for short. It"s a set of software tools and programs used by developers to create [applications](https://clevertap.com/glossary/app/) for specific platforms. SDK tools will include a range of things, including libraries, documentation, code samples, processes, and guides that developers can use and integrate into their own apps. SDKs are designed to be used for specific platforms or programming languages.

**Virtual Environment**

Use a virtual environment to manage the dependencies for your project, both in development and in production.

What problem does a virtual environment solve? The more Python projects you have, the more likely it is that you need to work with different versions of Python libraries, or even Python itself. Newer versions of libraries for one project can break compatibility in another project.

Virtual environments are independent groups of Python libraries, one for each project. Packages installed for one project will not affect other projects or the operating system"s packages.

Python comes bundled with the [venv](https://docs.python.org/3/library/venv.html#module-venv) module to create virtual environments.

**Create an environment**

Create a project folder and a venv folder within:

**macOS/LINUX**

```bash
$ mkdir myproject

$ cd myproject

$ python3 -m venv venv
```
**Windows**

```
 mkdir myproject

 cd myproject

 py -3 -m venv venv
```
**Activate the environment**

Before you work on your project, activate the corresponding environment:

**macOS/LINUX**

`$ . venv/bin/activate`

**Windows**

\&gt; venv\Scripts\activate

Your shell prompt will change to show the name of the activated environment.

**Install Lens**

Within the activated environment, use the following command to install Lens:

**$pip install lens-sdk**

**Getting Started With Lens API**

This Page will give you a good introduction to Lens. Before getting started with Lens, Follow Installation steps to install Lens.

Below are the code snippets to make a POST request and get the response back.

**\*Python\***
```python
import requests, json

url = "http://lensservice.polynomial.ai/kit/analyze"

payload = {
    "data": [
        {
            "user_id": 1543,
            "full_name": "Aparna Pothanis",
            "email": "aparnna_pothanis@polynomial.ai",
            "name": "Polynomial",
            "utterance": "Hi everyone",
            "identifier": 2,
            "start_time": "2021-10-19 18:00:55.760",
            "end_time": "2021-10-19 18:00:56.780",
        },
        {
            "user_id": 1543,
            "full_name": "Revant Amingad",
            "email": "ramingad@gainsight.com",
            "name": "Gainsight",
            "utterance": " Good afternoon.",
            "identifier": 3,
            "start_time": "2021-10-19 18:00:57.859",
            "end_time": "2021-10-19 18:01:01.250",
        },
    ]
}

headers = {"accesskey": "your_agent_key", "agentID": "your_agent_id"}

response = requests.post(url, headers=headers, data=json.dumps(payload))

print(response.text, response.status_code)

```
**\*\*cURL\*\***

curl --location --request POST "lensservice.polynomial.ai/kit/analyze" \

--header "accesskey: {{key}}" \

--header "agentID: 61b5efa89ef90206c8541bba" \

--data-raw "{

"data": [

{

"user\_id": 1543,

"full\_name": "Aparna Pothanis",

"email": "aparnna\_pothanis@polynomial.ai",

"name": "Polynomial",

"utterance": "Hi everyone",

"identifier": 2,

"start\_time": "2021-10-19 18:00:55.760",

"end\_time": "2021-10-19 18:00:56.780",

},

{

"user\_id": 1543,

"full\_name": "Revant Amingad",

"email": "ramingad@gainsight.com",

"name": "Gainsight",

"utterance": " Good afternoon.",

"identifier": 3,

"start\_time": "2021-10-19 18:00:57.859",

"end\_time": "2021-10-19 18:01:01.250",

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}"

**\*\*NodeJs - Native\*\***

var https = require("follow-redirects").https;

var fs = require("fs");

var options = {

"method": "POST",

"hostname": "lensservice.polynomial.ai",

"path": "/kit/analyze",

"headers": {

"accesskey": "{{key}}",

"agentID": "61b5efa89ef90206c8541bba"

},

"maxRedirects": 20

};

var req = https.request(options, function (res) {

var chunks = [];

res.on("data", function (chunk) {

chunks.push(chunk);

});

res.on("end", function (chunk) {

var body = Buffer.concat(chunks);

console.log(body.toString());

});

res.on("error", function (error) {

console.error(error);

});

});

var postData = "{

"data": [

{

"user\_id": 1543,

"full\_name": "Aparna Pothanis",

"email": "aparnna\_pothanis@polynomial.ai",

"name": "Polynomial",

"utterance": "Hi everyone",

"identifier": 2,

"start\_time": "2021-10-19 18:00:55.760",

"end\_time": "2021-10-19 18:00:56.780",

},

{

"user\_id": 1543,

"full\_name": "Revant Amingad",

"email": "ramingad@gainsight.com",

"name": "Gainsight",

"utterance": " Good afternoon.",

"identifier": 3,

"start\_time": "2021-10-19 18:00:57.859",

"end\_time": "2021-10-19 18:01:01.250",

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}"

req.write(postData);

req.end();

**\*\*NodeJs - Request\*\***

var request = require("request");

var options = {

"method": "POST",

"url": "lensservice.polynomial.ai/kit/kit/analyze",

"headers": {

"accesskey": "{{key}}",

"agentID": "61b5efa89ef90206c8541bba"

},

body: "{

"data": [

{

"user\_id": 1543,

"full\_name": "Aparna Pothanis",

"email": "aparnna\_pothanis@polynomial.ai",

"name": "Polynomial",

"utterance": "Hi everyone",

"identifier": 2,

"start\_time": "2021-10-19 18:00:55.760",

"end\_time": "2021-10-19 18:00:56.780",

},

{

"user\_id": 1543,

"full\_name": "Revant Amingad",

"email": "ramingad@gainsight.com",

"name": "Gainsight",

"utterance": " Good afternoon.",

"identifier": 3,

"start\_time": "2021-10-19 18:00:57.859",

"end\_time": "2021-10-19 18:01:01.250",

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}"

};

request(options, function (error, response) {

if (error) throw new Error(error);

console.log(response.body);

});

**Sample Request Json**

{

"data": [

{

"user\_id": 1543,

"full\_name": "Aparna Pothanis",

"email": "aparnna\_pothanis@polynomial.ai",

"name": "Polynomial",

"utterance": "Hi everyone",

"identifier": 2,

"start\_time": "2021-10-19 18:00:55.760",

"end\_time": "2021-10-19 18:00:56.780",

},

{

"user\_id": 1543,

"full\_name": "Revant Amingad",

"email": "ramingad@gainsight.com",

"name": "Gainsight",

"utterance": " Good afternoon.",

"identifier": 3,

"start\_time": "2021-10-19 18:00:57.859",

"end\_time": "2021-10-19 18:01:01.250",

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}

**Request Parameter**

**Header**

- accessKey : Unique key provided by the Agent
- agentID : Unique Id provided by the Agent

**Request Json**

- identifier : Unique utterance Id
- start\_time : Start time of the utterance
- end\_time : End time of the utterance
- utterance : Direct Utterance
- name : Name of the Organisation
- email : Email id of the speaker
- full\_name : Full name of the speaker
- user\_id : Host of the meeting

**Sample Response Json**

{

"prediction": {

"genderDistribution": {

"F": 111,

"M": 690

},

"genderLinguisticInsight": {

"M": {

"Accept": 97,

"Continuer": 47,

"Emphasis": 3,

"Greet": 9,

"Reject": 1,

"Statement": 479,

"System": 6,

"nAnswer": 3,

"whQuestion": 15,

"yAnswer": 18,

"ynQuestion": 12

},

"F": {

"Accept": 7,

"Continuer": 8,

"Greet": 1,

"Statement": 90,

"yAnswer": 5

}

}

}

}

**Response Json**

- genderDistribution : Count of Male/Female
- genderLinguisticInsight : Total count of Linguistic Insights of each gender.

**\*\*Note\*\* :** The response may vary according to the brains selected while agent creation.

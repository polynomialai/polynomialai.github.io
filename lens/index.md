**INSTALLATION**

**Python Version**

We recommend using python 3.7.

**What is an SDK?**

[SDK](https://clevertap.com/glossary/sdk/) stands for software development kit or devkit for short. It&#39;s a set of software tools and programs used by developers to create [applications](https://clevertap.com/glossary/app/) for specific platforms. SDK tools will include a range of things, including libraries, documentation, code samples, processes, and guides that developers can use and integrate into their own apps. SDKs are designed to be used for specific platforms or programming languages.

**Virtual Environment**

Use a virtual environment to manage the dependencies for your project, both in development and in production.

What problem does a virtual environment solve? The more Python projects you have, the more likely it is that you need to work with different versions of Python libraries, or even Python itself. Newer versions of libraries for one project can break compatibility in another project.

Virtual environments are independent groups of Python libraries, one for each project. Packages installed for one project will not affect other projects or the operating system&#39;s packages.

Python comes bundled with the [venv](https://docs.python.org/3/library/venv.html#module-venv) module to create virtual environments.

**Create an environment**

Create a project folder and a venv folder within:

**macOS/LINUX**

$ mkdir myproject

$ cd myproject

$ python3 -m venv venv

**Windows**

\&gt; mkdir myproject

\&gt; cd myproject

\&gt; py -3 -m venv venv

**Activate the environment**

Before you work on your project, activate the corresponding environment:

**macOS/LINUX**

$ . venv/bin/activate

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

import requests, json

url = &quot;http://lensservice.polynomial.ai/kit/analyze&quot;

payload={

&quot;data&quot;: [

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Aparna Pothanis&quot;,

&quot;email&quot;: &quot;aparnna\_pothanis@polynomial.ai&quot;,

&quot;name&quot;: &quot;Polynomial&quot;,

&quot;utterance&quot;: &quot;Hi everyone&quot;,

&quot;identifier&quot;: 2,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:55.760&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:00:56.780&quot;,

},

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Revant Amingad&quot;,

&quot;email&quot;: &quot;ramingad@gainsight.com&quot;,

&quot;name&quot;: &quot;Gainsight&quot;,

&quot;utterance&quot;: &quot; Good afternoon.&quot;,

&quot;identifier&quot;: 3,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:57.859&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:01:01.250&quot;,

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}

headers = {

&#39;accesskey&#39;: &#39;{{key}}&#39;

&#39;agentID&#39; : &#39;61b5efa89ef90206c8541bba&#39;

}​

response = requests.post(url, headers=headers, data=json.dumps(payload))

print(response.text , response.status\_code)

**\*\*cURL\*\***

curl --location --request POST &#39;lensservice.polynomial.ai/kit/analyze&#39; \

--header &#39;accesskey: {{key}}&#39; \

--header &#39;agentID: 61b5efa89ef90206c8541bba&#39; \

--data-raw &#39;{

&quot;data&quot;: [

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Aparna Pothanis&quot;,

&quot;email&quot;: &quot;aparnna\_pothanis@polynomial.ai&quot;,

&quot;name&quot;: &quot;Polynomial&quot;,

&quot;utterance&quot;: &quot;Hi everyone&quot;,

&quot;identifier&quot;: 2,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:55.760&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:00:56.780&quot;,

},

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Revant Amingad&quot;,

&quot;email&quot;: &quot;ramingad@gainsight.com&quot;,

&quot;name&quot;: &quot;Gainsight&quot;,

&quot;utterance&quot;: &quot; Good afternoon.&quot;,

&quot;identifier&quot;: 3,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:57.859&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:01:01.250&quot;,

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}&#39;

**\*\*NodeJs - Native\*\***

var https = require(&#39;follow-redirects&#39;).https;

var fs = require(&#39;fs&#39;);

var options = {

&#39;method&#39;: &#39;POST&#39;,

&#39;hostname&#39;: &#39;lensservice.polynomial.ai&#39;,

&#39;path&#39;: &#39;/kit/analyze&#39;,

&#39;headers&#39;: {

&#39;accesskey&#39;: &#39;{{key}}&#39;,

&#39;agentID&#39;: &#39;61b5efa89ef90206c8541bba&#39;

},

&#39;maxRedirects&#39;: 20

};

var req = https.request(options, function (res) {

var chunks = [];

res.on(&quot;data&quot;, function (chunk) {

chunks.push(chunk);

});

res.on(&quot;end&quot;, function (chunk) {

var body = Buffer.concat(chunks);

console.log(body.toString());

});

res.on(&quot;error&quot;, function (error) {

console.error(error);

});

});

var postData = &#39;{

&quot;data&quot;: [

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Aparna Pothanis&quot;,

&quot;email&quot;: &quot;aparnna\_pothanis@polynomial.ai&quot;,

&quot;name&quot;: &quot;Polynomial&quot;,

&quot;utterance&quot;: &quot;Hi everyone&quot;,

&quot;identifier&quot;: 2,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:55.760&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:00:56.780&quot;,

},

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Revant Amingad&quot;,

&quot;email&quot;: &quot;ramingad@gainsight.com&quot;,

&quot;name&quot;: &quot;Gainsight&quot;,

&quot;utterance&quot;: &quot; Good afternoon.&quot;,

&quot;identifier&quot;: 3,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:57.859&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:01:01.250&quot;,

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}&#39;

req.write(postData);

req.end();

**\*\*NodeJs - Request\*\***

var request = require(&#39;request&#39;);

var options = {

&#39;method&#39;: &#39;POST&#39;,

&#39;url&#39;: &#39;lensservice.polynomial.ai/kit/kit/analyze&#39;,

&#39;headers&#39;: {

&#39;accesskey&#39;: &#39;{{key}}&#39;,

&#39;agentID&#39;: &#39;61b5efa89ef90206c8541bba&#39;

},

body: &#39;{

&quot;data&quot;: [

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Aparna Pothanis&quot;,

&quot;email&quot;: &quot;aparnna\_pothanis@polynomial.ai&quot;,

&quot;name&quot;: &quot;Polynomial&quot;,

&quot;utterance&quot;: &quot;Hi everyone&quot;,

&quot;identifier&quot;: 2,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:55.760&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:00:56.780&quot;,

},

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Revant Amingad&quot;,

&quot;email&quot;: &quot;ramingad@gainsight.com&quot;,

&quot;name&quot;: &quot;Gainsight&quot;,

&quot;utterance&quot;: &quot; Good afternoon.&quot;,

&quot;identifier&quot;: 3,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:57.859&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:01:01.250&quot;,

},

{\&lt;-\&gt;},

{\&lt;-\&gt;}

]

}&#39;

};

request(options, function (error, response) {

if (error) throw new Error(error);

console.log(response.body);

});

**Sample Request Json**

{

&quot;data&quot;: [

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Aparna Pothanis&quot;,

&quot;email&quot;: &quot;aparnna\_pothanis@polynomial.ai&quot;,

&quot;name&quot;: &quot;Polynomial&quot;,

&quot;utterance&quot;: &quot;Hi everyone&quot;,

&quot;identifier&quot;: 2,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:55.760&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:00:56.780&quot;,

},

{

&quot;user\_id&quot;: 1543,

&quot;full\_name&quot;: &quot;Revant Amingad&quot;,

&quot;email&quot;: &quot;ramingad@gainsight.com&quot;,

&quot;name&quot;: &quot;Gainsight&quot;,

&quot;utterance&quot;: &quot; Good afternoon.&quot;,

&quot;identifier&quot;: 3,

&quot;start\_time&quot;: &quot;2021-10-19 18:00:57.859&quot;,

&quot;end\_time&quot;: &quot;2021-10-19 18:01:01.250&quot;,

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

&quot;prediction&quot;: {

&quot;genderDistribution&quot;: {

&quot;F&quot;: 111,

&quot;M&quot;: 690

},

&quot;genderLinguisticInsight&quot;: {

&quot;M&quot;: {

&quot;Accept&quot;: 97,

&quot;Continuer&quot;: 47,

&quot;Emphasis&quot;: 3,

&quot;Greet&quot;: 9,

&quot;Reject&quot;: 1,

&quot;Statement&quot;: 479,

&quot;System&quot;: 6,

&quot;nAnswer&quot;: 3,

&quot;whQuestion&quot;: 15,

&quot;yAnswer&quot;: 18,

&quot;ynQuestion&quot;: 12

},

&quot;F&quot;: {

&quot;Accept&quot;: 7,

&quot;Continuer&quot;: 8,

&quot;Greet&quot;: 1,

&quot;Statement&quot;: 90,

&quot;yAnswer&quot;: 5

}

}

}

}

**Response Json**

- genderDistribution : Count of Male/Female
- genderLinguisticInsight : Total count of Linguistic Insights of each gender.

**\*\*Note\*\* :** The response may vary according to the brains selected while agent creation.

# Read: Class 16 
## Serverless Functions


>1- What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?

Serverless computing is a cloud computing model that allows developers to build and run applications without the need to manage traditional server infrastructure. Here are the key characteristics of serverless computing and how it differs from traditional server-based architectures:

No Server Management: In serverless computing, the cloud provider is responsible for managing the underlying infrastructure. Developers can focus solely on writing code without worrying about provisioning, scaling, or maintaining servers.

Event-Driven Execution: Serverless architectures are event-driven, meaning that functions (also known as serverless functions or FaaS functions) are triggered by specific events or requests. Functions are executed in response to events such as HTTP requests, database changes, file uploads, or scheduled tasks.

Automatic Scaling: Serverless platforms automatically scale the execution environment based on the incoming workload. Each function is isolated and runs independently, and the cloud provider dynamically provisions resources as needed. This allows applications to handle fluctuating workloads without manual intervention.

Compared to traditional server-based architectures, serverless computing offers several advantages:

a. Reduced Operational Complexity: With serverless, you offload infrastructure management to the cloud provider, reducing operational overhead and allowing developers to focus on application logic.

b. Improved Scalability: Serverless platforms automatically scale resources up or down based on demand, providing seamless scalability without manual intervention or capacity planning.

c. Cost Efficiency: Pay-per-use pricing in serverless computing ensures that you only pay for the actual execution time, eliminating costs for idle resources.




>2-How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?

o get started with Vercel, follow these steps:

Sign up: Visit the Vercel website (vercel.com) and sign up for a free account. You can sign up using your GitHub, GitLab, or Bitbucket account.

Install the Vercel CLI (Command-Line Interface): The Vercel CLI allows you to deploy and manage projects from your local development environment. Install the CLI by running the appropriate command for your operating system, as provided in the Vercel documentation.

Set up your project: Navigate to your project's directory using the command line. Ensure that your project has the necessary configuration files, such as package.json for Node.js projects.

Login to Vercel: Run the vercel login command in your project directory to authenticate your Vercel account with the CLI. Follow the instructions provided to complete the login process.

Deploy a serverless function: To deploy a serverless function using Vercel, you need to create an API endpoint that triggers your function

Follow these steps:

a. Create a serverless function: In your project directory, create a new directory named api. Inside this directory, create a JavaScript or TypeScript file that exports a function. This function will be your serverless function.

javascriptCopy code
// Example serverless function module.exports = (req, res) => { res.status(200).json({ message: 'Hello, serverless!' }); };

b. Create an API route: In your api directory, create an index.js or index.ts file. This file will define the API route and associate it with your serverless function.

javascriptCopy code
// Example API route module.exports = (req, res) => { if (req.method === 'GET') { // Invoke your serverless function for GET requests return require('./your-serverless-function.js')(req, res); } else { res.status(405).end(); // Method Not Allowed } };

c. Deploy the function: Use the Vercel CLI to deploy your project by running vercel. It will guide you through the deployment process and provide you with a URL for your deployed serverless function.




>3-What are APIs, and how can they be utilized in Python applications to access and manipulate data from external sources?

API stands for Application Programming Interface. It is a set of rules and protocols that allows different software applications to communicate and interact with each other. APIs enable developers to access and manipulate data or functionality provided by external systems, such as web services, databases, or online platforms.

In Python applications, APIs can be utilized to access and manipulate data from external sources by making HTTP requests and processing the responses. Here's a general process for utilizing APIs in Python:

Import the necessary libraries: In your Python application, import the required libraries for making HTTP requests and handling responses. The popular libraries for this purpose are requests and json.

import requests
import json


 2.Make an HTTP request to the API: Use the requests library to send an HTTP request to the API endpoint. Specify the URL of the API and any required parameters or headers.

response = requests.get(url, params=params, headers=headers)

Handle the response: Once you receive the response from the API, you can access the data returned by the API and perform any necessary data manipulation. The response is typically in JSON format, so you can use the json library to parse the response.

data = response.json()





>4-What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?

The Requests library is a popular Python library used for making HTTP requests and interacting with APIs. It provides a simple and intuitive interface to send various types of HTTP requests such as GET, POST, PUT, DELETE, and more. The library abstracts away the complexities of making HTTP requests and handling responses, allowing developers to interact with APIs easily.

To use the Requests library, you first need to install it. You can install it using pip by running the following command:

pip install requests


Once installed, you can import the library in your Python script using the following line:

import requests
Ex:
```py
import requests

# Send a GET request to a URL
response = requests.get('https://api.example.com/endpoint')

# Check the response status code
if response.status_code == 200:
    # Successful request
    data = response.json()  # Parse the response as JSON
    # Process and use the response data as needed
    print(data)
else:
    # Request was not successful
    print('Request failed with status code:', response.status_code)
```




## Sources:

https://www.datacamp.com/tutorial/making-http-requests-in-python

https://realpython.com/api-integration-in-python/



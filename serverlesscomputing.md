# Serverless Computing
 
| Name | Durga Mane|  
| ----------- | ----------- |  

## 1. Serverless Computing

### 1.1 What is serverless computing?


Serverless computing is a way for developers to create and run programs without worrying about the technical stuff behind the scenes. Even though it's called ***serverless*** there are still servers working in the background, but developers don't need to deal with them directly. Instead, they can just focus on writing their code and making their apps work. The cloud service provider takes care of all the heavy lifting, like managing the servers and making sure everything runs smoothly. It's like having a team of helpers handling the technical details while developers focus on creating awesome applications that automatically adjust to handle more users or work as needed.


![alt text](https://github.com/durgamane12/Images/blob/main/servgerless.png?raw=true)

### 1.2 Benefits of Serverless architecture

####  **Reduced Operational Overhead:**

Serverless computing frees developers from tasks like server provisioning, maintenance, and scaling, allowing them to focus on writing code and delivering value.

####  **Scalability and Flexibility:**

Applications hosted in a serverless environment can automatically scale to handle varying workloads, ensuring optimal performance without manual intervention.

####  **Cost Efficiency:**

Serverless architectures often follow a pay-per-use pricing model, where users are charged based on the resources consumed by their functions or applications. This can result in cost savings as you only pay for what you use.

####  **High Availability:**

Cloud providers ensure high availability by managing the underlying infrastructure. Functions or applications deployed in a serverless environment benefit from built-in redundancy and fault tolerance.

####  **Faster Time-to-Market:**

With reduced infrastructure concerns, developers can deploy code faster, iterate more quickly, and deliver features to users in shorter cycles.


### 1.3 Use Cases

#### Web Applications:

Serverless computing is well-suited for building web applications, handling HTTP requests and responding dynamically to user interactions.

#### Real-time Data Processing:

It's effective for processing real-time streaming data from sources like IoT devices or event-based systems.

#### Scheduled Tasks and Cron Jobs:

Serverless enables the execution of periodic tasks and scheduled jobs without the need for maintaining a dedicated server.

#### Automation and Orchestration:

Serverless functions can automate workflows and orchestrate processes by responding to events across different systems and services.

***Serverless computing offers a versatile architecture*** that fits various use cases, providing scalability, cost-effectiveness, and agility to developers and businesses.

## 2. Serverless Basics

### Functions as a Service (FaaS):

In serverless, FaaS means breaking tasks into small, standalone functions. Each function does a specific job, like handling an incoming message or processing data. Instead of managing the whole app, developers focus on writing these smaller, task-oriented functions.

### Events and Triggers:

Events are things that happen, like a user clicking a button or a file being uploaded. ***Triggers are what start these events***. For example, a click triggers a function to run. Triggers can be anything that makes a function start working.

The ***HTTP trigger lets you invoke a function with an HTTP request***. You can use an HTTP trigger to build serverless APIs and respond to webhooks.

The default return value for an HTTP-triggered function is:

-   `HTTP 204 No Content`  with an empty body in Functions 2.x and higher
-   `HTTP 200 OK`  with an empty body in Functions 1.x

### Scaling and Concurrency:

Serverless adjusts automatically to handle more work when needed. If many people start using an app, the serverless system gets more resources to manage the extra workload. Concurrency means that multiple functions can work at the same time, so even if lots of things are happening at once, the system can handle it smoothly.

## 3. Azure functions serverless computing

Azure Functions is an event-driven, serverless compute platform that helps you develop more efficiently using the programming language of your choice. Focus on core business logic with the highest level of hardware abstraction. Simplify complex orchestration challenges, build and debug locally, deploy at scale in the cloud, and connect functions to Azure services using triggers and bindings.

### 3.1 Azure Functions

Azure functions provide a serverless compute experience. A ***function is invoked by a  _trigger_  (such as access to an HTTP endpoint or a timer) and executes a block of code or business logic***. Functions also support specialized  _bindings_  that connect to resources like storage and queues.




![alt text](https://github.com/durgamane12/Images/blob/main/azurefunction.png?raw=true)

### 3.2  App service plans

Functions are backed by an  _app service plan_. The plan defines the resources used by the functions app. You can assign plans to a region, determine the size and number of virtual machines that will be used, and pick a pricing tier. For a true serverless approach, ***function apps may use the consumption plan***. The consumption plan will scale the back end automatically based on load.

### 3.3 Application Insights
Azure Application Insights is a comprehensive ***application performance management (APM)*** service offered by Microsoft Azure. It's designed to help developers and administrators monitor, diagnose, and gain insights into the performance and usage of their applications. You can turn on Application Insights for function apps simply by flipping a switch in the portal. Application Insights provides all of these capabilities without you having to configure a server or set up your own database. All of Application Insights' capabilities are provided as a service that automatically integrates with your apps.


### Steps:
Basic steps to syncing data from an offline database to online table storage using Azure Functions in Visual Studio:

#### 1. Set Up Azure Storage Account:
   - Create an Azure Storage Account where you want to sync your data. Note down the connection string for this storage account.

#### 2. Create an Azure Function Project:
   - Open Visual Studio and create a new Azure Functions project.
   - Choose a suitable trigger for your function (e.g., Timer trigger or Database trigger).

#### 3. Add Required NuGet Packages:
   - If your offline database requires a specific client library (e.g., SQL Server, MongoDB), add the necessary NuGet packages to your project to interact with this database.

#### 4. Connect to the Offline Database:
   - Write code within your Azure Function to connect to the offline database. Use the appropriate database client library and credentials to establish a connection.

#### 5. Retrieve Data from the Offline Database:
   - Fetch the data you want to sync from the offline database. This might involve running SQL queries or using other database-specific retrieval methods.

#### 6. Connect to Azure Table Storage:
   - Use the Azure Storage SDK or client library to connect to the Azure Table Storage account you set up earlier. Use the connection string to authenticate and access the storage.

#### 7. Transform and Upload Data to Azure Table Storage:
   - Process the data retrieved from the offline database as needed (e.g., transform it into the format required by Azure Table Storage).
   - Upload the data to the Azure Table Storage by creating entities and inserting them into the appropriate table(s).

#### 8. Test and Deploy the Azure Function:
   - Test your Azure Function locally to ensure it works as expected by triggering it and checking for data synchronization.
   - Publish or deploy the Azure Function to your Azure account so that it runs in the cloud according to your specified trigger (e.g., on a schedule or in response to a database change).

#### 9. Monitor and Maintain:
   - Monitor the Azure Function to ensure it's syncing data correctly and without errors.
   - Implement error handling and logging mechanisms to troubleshoot and maintain the synchronization process.

Remember, the specifics of connecting to your offline database, retrieving data, and interacting with Azure Table Storage will depend on the type of databases you're using and the structure of your data.

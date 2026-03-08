# AI and ML
## Artificial Intelligence (AI)
- A broad field focused on the development of intelligent computer systems capable of performing humanlike tasks.
## Machine Learning (ML)
- Training machines to perform complex tasks without explicit instructions.
- Finds the patterns hidden in vast amounts of data to produce a model.
- The model can then be applied to new data to make predictions based on what it learned.
  
<b> AI & ML -> Train -> ML Model -> Predictions </b>

## Common ML business use cases
- Powers the Amazon e-commerce recommendations engine.
- Predict trends, such as future stock prices.
- Decision making, such as routing callers to the right department.
- Detect anomalies, like bank fraud.

## AWS AI/ML solutions
- AI Services
  - Pre-built models already trained to perform specific functions.
- ML Services
  - More customized approach with Amazon SageMaker AI. You build, train, and deploy your own ML Model with fully managed infrastructure.
- ML Frameworks & Infrastructure
  - A completely custom building model using purpose-built chips that integrate with popular ML frameworks.
 
# AWS Tiers
## Tier 1: Pre-build AWS AI services
- Made up of pre-build models that are already trained to do specific functions making them ready to use.
### Language services
Great for interpreting text or speech, then transforming it into something meaningful.
- Amazon Comprehend
  - Uses natural language processing to extract key insights from documents. Good for content classificatoin, customer sentiment analysis, and compliance monitoring.  
- Amazon Polly
  - Converts text into lifelike speech. Supports multiple languages, different genders, and different accents. Used in virtual assistants, e-learning applications, and accessibility enhancements for visually impaired users.
- Amazon Transcribe
  - Converts speech to text. Supports multiple languages, and has speaker identification, custom vocabulary, and real-time transcription. Good for customer call transcription, automated subtitling, and metadata generation for media content.
- Amazon Translate
  - Real-time and batch text translation across multiple languagues. Used in document translation, and multi-language applicatoin integrations.

### Computer Vision and Search Services
- Amazon Kendra
  - Uses natural language processing to search for answers within large amounts of enterprise content. It understands the context of a query. Good for intelligent search, chatbots, and application search integration.
- Amazon Rekognition
  - Video analysis service. It can identify objects, people, text, scenes, and activities within images and videos stored in Amazon S3. Good for content moderation, identity verification, media analysis, and home automation experiences.
- Amazon Textract
  - Detects and extracts typed and handwritten text found in documents, forms, and even tables within documents. Used for financial, healthcare, and government form text extraction for quick processing.
 
### Conversational AI and Personalization Services
Users can interact with apps through text, and voice conversations.

- Amazon Lex
  - You can add voice and text convesational interfaces to your applications. This service uses both natural language understanding and automatic speech recognition to create lifelike conversations. Used by virtual assistants, natural language search for FAQs, and automated application bots.
-Amazon Personalize
  - You can use historical data to build intelligent applications with personalized recommendations for your customers. Used in personalized streaming, product, and trending recommendations.

## Tier 2: ML Services
Provides a more customized approach for customers who want a bit more control over their ML solutions without having to manage infrastructure. SageMaker AI is a key offering in this tier.

### Amazon SageMakerAI
- Build, train, deploy your own ML models without worrying about infrastructure. Has an IDE providing simplified access control and transparency over your ML projects.

Benefits of using SageMaker AI
- Increase innovation with different tool choices. Data scientists can use the IDE, and business analysts cn use the no-code interface.
- Fully managed infrastructure allowing you to focus on your ML model deployment.
- You can automate and standardize your MLOps practices across enterprises to support transparency and audability.

## Tier 3: ML Frameworks & Infrastructure
Some organizations have highly specialized needs that require complete control over the ML training process.
- ML Frameworks
  - A software library or tool that provides experienced ML practitioners with pre-built, optimized components for building machine models. AWS supports ML frameworks like PyTorch, Apache M-X Net, and TensorFlow.
- AWS ML Infrastructure
  - Provides high performance and flexibility for advanced ML workloads. AWS serves ML-optimized EC2, Amazon EMR, and Amazon ECS for this.
 
# Generative AI on AWS
## Deep Learning
- A subset of machine learning where models are trained using layers of artificial neurons that mimic the human brain. Each layer of these neural networks summarizes and feeds information to the next layer until a final model is produced.
  
## Generative AI
- A type of deep learning powered by extremely large ML models known as foundation models (FMs). FMs are pre-trained on vast collections of data. They can be adapted to perform multiple tasks in comparison to traditional ML models.
- Large language models (LLMs), are a popular type of FM trained to use human language (ChatGPT, Gemini, Claude). They can also be used to create videos, images, music, and more.

# Types of AWS Gen AI
## Amazon SageMaker JumpStart
- An ML hub with FMs and pre-built ML solutions deployable with a few clicks.
- Use cases:
  - Quickly deploy pre-trained models without extensive ML expertise.
  - Fine-tune pre-trained FMs with your domain-specific data
  - Compare performance for different models before commiting to a specific approach.

## Amazon Bedrock
- A fully managed service for adapting and deploying FMs from Amazon and other leading AI companies.
- Use cases:
  - Build production-ready generative AI applications with enterprise-level security, privacy, and scalability.
  - Create applications that can generate multiple content types, such as text and images.
  - Develop advanced conversational agents that connect to your enterprise data to provide accurate responses.
    
## Amazon Q
- An interactive AI assistant that can be integrated with a company's information repositories.
- Amazon Q Business:
  - Can answer pressing questions, help solve problems, and take actions using the data and expertise found in your company's information repositories. It provides information requests, automated workflows, and insight extraction.
- Amazon Q Developer:
  - It provides code recommendations to accelerate development for coding languages like C#, Java, JavaScript, Python, and TypeScript applications. It has faster code generation, improved reliability, and automated code reviews.
 
# Data Analytics
## Data Pipelines for ETL Processes
1. <b>E</b>xtract the data from various sources and store it.
2. <b>T</b>ransform it into a consistent, usable format for downstream tools to consume.
3. <b>L</b>oad it into a destination system, like a data warehouse or analytics platform.

## Data Analytics
It is the process where analysts transforms raw historical data to uncover valuable insights and trends. The use cases are:
1. Loan companies explaining lending decisionst to customers.
2. Medical researchers analyzing clinical trial data through hypothesis testing.
3. Insurance companies making their risk assessment models transparent for regulators.

# AWS Data Pipeline
## Data Ingestion Services
This involves moving data from source systems into your chosen storage solution. Use real-time ingestion when the data is needed immediately. Use batch ingestion when some latency is tolerable.

### Amazon Kinesis Data Streams
- Used for real-time ingestion of TBs of data from apps, streams, and sensors. This serverless service even provides automatic provisioning ad scaling on demand.

### Amazon Data Firehose
- Option for data ingestion in NEAR real-time. This is a fully managed service that provides automatic provisioning and scaling. It delivers data within seconds to data lakes, warehouses, and analytic services.

## Data Storage Services
Data can come from many different sources. To gain insights, data is commonly consolidated into a single location. There are two storage options for this. Flexible data lakes store vast amounts of raw data. Alternatively, the more structured data warehouses are optimized for business intelligence.

### Amazon S3
- A popular choice for data lakes. An object storage service that can securely house virtually any amount of structured or unstructured data. Fully elastic, automatically scaling when data is added and removed.

### Amazon Redshift
- A fully managed data warehouse service that can store petabytes of structured or semistructured data. With the scalability and pay-as-you-go pricing model, organizations can cost-effectively analyze large datasets.

## Data Cataloging Services
Cataloging your data with metadata provides an inventory of your organization's data.
### AWS Glue Data Catalog
- Provides a centralized, scalable, and managed metadata repository that enhances data discovery. It improves the overall efficiency of data pipelines by delivering metadata to various data stores and analytics services.

## Data Processing Services
Cleans and transforms data so it's ready to analyze.
### AWS Glue
- A fully managed ETL service that makes data preparation simpler, faster, and cost effective. AWS Glue ETL jobs can use the AWS Glue Data Catalog to access metadata about data sources, which can help inform transformations defined in the ETL script.
### Amazon EMR
- Ideal for large-scale data processing and organizations with existing big data expertise. It automatically handles infrastructure provisioning, cluster management, and scaling. EMR supports popular big data frameworks like Apache Spark, Apache Hadoop, and Apache Hive.

## Data Analysis and Visualization Services
These are tools that help you develop important isights about your data.
### Amazon Athena
- You can run SQL queries in this fully managed serverless service to analyze data in relational, nonrelational, object, and custom data sources hosted on Amazon S3, on premises, or even in multi-cloud environments. You only pay for the queries you run, making this a cost effective solution.

### Amazon Redshift
- A fully managed data warehouse solution. Its columnar storage and massively parallel processing architecture make it ideal for analyzing large datasets. It is used for performing complex SQL queries on large datasets for frequent, high-performance analytical workloads.

### Amazon QuickSight
- Both technical and non-technical users can quickly create modern interactive dashboards and reports from various data sources without managing infrastructure.
- Provides natural language queries so buisness analysts and users can build, discover, and share meaningful insights in seconds.

### Amazon OpenSearch Service
- Can search for relevant content through precise keyword matching or natural language queries. Unified dashboards provide real-time data visualization as you analyze and monitor logs, traces, and metrics for various applications.

# Data Analytics and AI/ML Flow
1. <b>Make Recommendations:</b> An e-commerce company uses an ML model to make product recommendations.
2. <b>Store App Data:</b> Amazon DynamoDB stores the historical customer data gathered through the app. This makes sense for low latency reads and writes but isn't ideal for ML model training.
3. <b>Ingest Data:</b> Kinesis Data Streams ingests the data from DynamoDB. Amazon Data Firehose then aggregates the data.
4. <b>Proces data:</b> The data is in JSON format, so Firehose invokes an AWS Lambda function that transforms the data into .csv format.
5. <b>Deliver Data:</b> Firehose then delivers the data to the company's Amazon S3 data lake, where it is available for multiple consumers.
6. <b>Catalog Data:</b> AWS Glue Data Catalog serves as a metadata repository with tables that describe the schema and location of the Amazon S3 data.
7. <b>Perform Data Analytics:</b> Data scientists use Athena to gather insights through queries.
8. <b>Train Model:</b> SageMaker AI reads the same dataset directly from Amazon S3. ML engineers can then train new versions of the recommendation model using the latest information.

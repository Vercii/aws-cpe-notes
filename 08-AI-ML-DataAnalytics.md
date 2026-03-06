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

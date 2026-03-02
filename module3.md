AWS offers both unmanaged and managed services allowing the customers to have different levels of responsibility and control based on what they need, and their liking.

## Unmanaged Services
- AWS takes care of the underlying physical infrastructure
- Customer is responsible for setting up, securing, and maintaining the OS, network configurations, and applications on their instances.

## Managed Services
- AWS handles much of the operational overhead, giving the customer less responsibility.
- Customers need to perform less provisioning compared to unmanaged services.

## Fully-managed services
- Eliminates the need for customer to provision or manage servers.
- The infrastructure, scalability, and availability are all handled by AWS, allowing customers can focus entirely on writing and deploying code. 
- Also known as serverless.

## AWS Lambda
- Serverless compute service that runs code without the need to provision or manage servers.
- Underlying infrastructure is automatically managed, resources are scaled based on the volume of requests.
- Memory size can be configured in order to optimize performance.

Lambda use cases:
- Real-time image processing for a social media application
	- When users upload images, Lambda is triggered to resize the image, and save it to storage in an optimized format. The number of uploads is what Lambda scales on, and charges only for the time spent processing the images.
- Event handling for an online game
	- Lambda handles real-time game events like player actions, leader board updates, and game state changes. Lambda is triggered every time an event happens like scoring a point or unlocking an achievement, automatically updating the player data and game status.

Key Components of Lambda:
- Function: Instructions for when an event is triggered.
- Triggers: The signal in which a function should be called.
- Runtime: The language environment used to run the function (e.g., Node.js, Python, Java).

## Containers
- Packages the application so it works the same on any computer, easing the process of moving, updating, and managing.
- Solves deployment fails by keeping the app's environment cosistent everywhere, making deployments smoother.
- Faster and lighter than Virtual Machines (VM) because the host's computer operating system is shared.

## Virtual Machine
- Uses a hypervisor to run full, separate OS, making them less resource-efficient with longer startup times compared to containers.

## Orchestration
- Automates deployment, scaling, and management. Useful for situations where containers reach the hundreds or thousands across multiple hosts, making them scale big and become too complex to manually handle.

## Amazon Elastic Container Service (ECS)
- A scalable container orchestration service for running and managing containers on AWS.

Launch Types: <br>
1. <b>ECS with EC2:</b> Ideal for small or medium businesses that need full control over infrastructure. Useful for custom applications with specific hardware or networking configurations. <br>
2. <b>ECS with Fargate:</b> A serverless option, meaning no server management required. Allowing teams to focus on development while Amazon ECS handles the scaling and orchestration. This is perfect for startups building web apps with variable traffic. <br>

## Amazon Elastic Kubernetes Service (EKS)
- Vanilla Kubernete is an open-source application, mostly known as a service too complex for beginners. Amazon EKS makes this easier by providing a fully managed service dedicated to running Kubernetes on AWS. Deploying, managing, and scaling containerized apps using open source Kubernetes are all simplified.

Launch Types: <br>
1. <b>EKS with EC2:</b> Best for companies needing full control over infrastructure. Offering deep customization of EC2 instances with Kubernetes scalability. Ideal for complex, and large-scale workloads. <br>
2. <b>EKS with Fargate:</b> Best for implementing Kubernetes flexibilitiy without managing the servers. It combines Kubernetes power with serveerless simplicity. <br>

## Amazon Elastic Container Registry (ECR)
- The storage itself where container images are managed, and deployed. You may push, pull, and manage images in ECR using standard container tools, and command line interfaces (CLI).

## Fargate
- Serverless compute engine for containers, removing the need to manage servers. Works both with ECS, and EKS.

## Elastic Beanstalk
- Fully managed service that streamlines the deployment, management, and scaling of web applications by automatically handling the provisioning of infrastructure, scaling, load balancing, and application health monitoring.
- Supports different PLs and frameworks such as Java, Python, Node.js, Docker, and more.

## AWS Batch
- Fully managed service that runs batch computing workloads. It automatically schedules, manages, and scales compute resources for batch jobs. Good for processing large-scale, parallel workloads in areas like scientific computing, media transcoding, and machine learning training.

## Lightsail
- Cloud service offering virtual private servers (VPSs), storage, databases, and networking at a predictable monthly price. Ideal for basic web application, low-traffic websites, testing environments, and learning cloud services.

## Outposts
- Fully managed hybrid cloud solution that combines AWS infrastructure with on-premises data centers, providing a consistent experience between on premises and AWS Cloud. Good for low-latency applications, data processing in remote locations, and modernizing legacy applications.

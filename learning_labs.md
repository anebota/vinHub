# Websites URL:
## DevOps Lifecycle Overview:
DevOps is a practice that enables a single team to handle the whole application lifecycle, including development, testing, release, deployment, operation, display, and planning. It is a mix of the terms “Dev” (for development) and “Ops” (for operations). We can speed up the delivery of applications and services by a business with the aid of DevOps. Amazon, Netflix, and other businesses have all effectively embraced DevOps to improve their customer experience.
![Architecture Diagram](https://media.geeksforgeeks.org/wp-content/uploads/20230412162703/DevOps-lifecycle.webp)
### DevOps Lifecycle: [Click to Open DevOps LifeCycle](https://www.geeksforgeeks.org/devops-lifecycle/) 

## 3tier Architecture Overview:
![Architecture Diagram](https://static.us-east-1.prod.workshops.aws/public/deeaf148-5f5f-4eac-ae36-a029faa8e4ba/static/introduction/3TierArch.png)

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

### AWS 3Tier Web Architecture: [Click to open AWS 3Tier Web Architecture](https://catalog.us-east-1.prod.workshops.aws/workshops/85cd2bb2-7f79-4e96-bdee-8078e469752a/en-US)


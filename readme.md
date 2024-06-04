
# Spring PetClinic with CI Pipeline and JFrog Artifactory Repository Demo

Requirement : 

Task - Build a pipeline:
1. Use Spring pet-clinic (https://github.com/spring-projects/spring-petclinic) as your project source code
2. Build a GitHub Actions pipeline with the following steps:

   -Compile the code

   -Run the tests

   -Package the project as a runnable Docker image

   -Publish the image to JFrog Artifactory in your pipeline
   
3. Make sure all dependencies are resolved from Maven Central


Deliverables:

1. GitHub link to the repo including

    -GitHub Actions workflow files within that repo
  
    -Docker file within that repo
  
    -readme.md file explaining the work and how to run the project
  
    -Bonus Deliverable: XRay Scan Data export (JSON format) for your image
  
2. Command to obtain and run the docker image

Answer:
1. Github Actions workflow files : /.github/workflows/main.yml
2. Jfrog Artifactory image URL : mickeyfan.jfrog.io/petclinic/spring-petclinic:3.3.0-SNAPSHOT
3. Docker file : using spring boot plugin, we can build the image without using docker file. e.g. ./mvnw spring-boot:build-image, developer don't need to maintain the Docker file
4. readme.md : /readme.md
5. Xray Scan data export : / xray-scan-results/*

## Steps to run the project




1. Clone the repository:
   git clone https://github.com/mfan28sydney/spring-petclinic-demo.git
   cd spring-petclinic

2. Build the Docker image:
   docker build -t petclinic:latest .

3. Run the Docker container:
   docker run -p 8080:8080 petclinic:latest

4. Access the application at http://localhost:8080.

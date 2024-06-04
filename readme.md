
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
1. Github Repo
   - Githuhttps://github.com/mfan28sydney/spring-petclinic
   - Github Actions workflow files : /.github/workflows/main.yml
   - Jfrog Artifactory image URL : mickeyfan.jfrog.io/petclinic/spring-petclinic:3.3.0-SNAPSHOT
   - Docker file : using spring boot plugin, we can build the image without using docker file. e.g. ./mvnw spring-boot:build-image, developer don't need to maintain the Docker file
   - readme.md : /readme.md
   - Xray Scan data export : / xray-scan-results/*
2. Command to obtain the docker image
   docker pull mickeyfan.jfrog.io/petclinic/spring-petclinic:3.3.0-SNAPSHOT



# DevSecOps
Below mentioned is the different steps implemented to build the complete CI/CD Pipeline 
Below is mentioned the different stage in the pipeline 

Input : Git Code 

1.Build & Unit test 
2.Code coverage
3.SCA
4.SAST
5.Quality Gates
6.Build Image 
7.Scan Image 
8.Smoke Test

Output : Docker Image 

1.Build & Unit test {Tool: Maven} - Generate Artifact (Converting the source code to product ) & Unit Test (Testing entire code together to check the integrity of the code ) 

2.Code Coverage { Tool : Jacoco} - Making sure the entire code is working and all the required actions are working as expected & Also shows junk and unused code 

3.SCA (Static analysis/Software composition analysis) {Tool: OWASP Dependency check} - Identify Vulnerabilities introduced by open-source or 3rd party liberties used in code 

4.SAST (Static Application Security testing ){Tool: Sonarqube Scanner}- Without running the application we scan the code and check if it has any vulnerabilities, check the coding practice has been followed. 

5.Quality Gate { Tool : Sonarqube Quality Profile} - Check if application meets the quality standards (code coverage > 98% .,etc)

6.Build Docker Image {Tool: Dockerfile} - Generate Deployable Artifact (Docker Image)

7.Scan Image {Tool : Trivy} - Identify Vulnerabilities in image Layer / Scan the Docker 
image for Vulnerabilities 

8.Smoke Test {Tool:Docker Container } - Testing the built image is working as expected 




Prereq : Create Two EC2 Server 
* Make using Terraform 
1.“Build Server ” - 15GB Storage - T2.micro
2.“Sonarqube Server ” - 4GB Memory - T2.medium 
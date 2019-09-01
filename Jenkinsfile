node {
   
   stage('Code Checkout') { 
     git credentialsId: 'githubID', url: 'https://github.com/itrainjaquar/maven-examples.git'
     
    }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
      sh 'mvn clean compile'
      }
    }
   stage('Unit Test run') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn test'
      } 
    }
   stage('Sonarqube analysis'){
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
      sh 'mvn sonar:sonar \
         -Dsonar.projectKey=Maven-ManiJ \
         -Dsonar.organization=manikandance \
         -Dsonar.host.url=https://sonarcloud.io \
         -Dsonar.login=7e592513b29732f6a0761be438e29ee88e3d1a6e'
       }  
    }
  stage("Quality Gate"){
          
    }
   stage('Package to Jfrog') {
    
    }
   
   stage('Deploy to Dev') {
     
    }
   stage('Automation Testing') {
     
    }
   stage('Deploy to Test') {
     
    }
   stage('Smoke Testing') {
     
    }
   stage('Deploy to Prod') {
     
    }
   stage('Acceptance Testing') {
     
    }
}

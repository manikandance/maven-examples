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
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
      sh 'mvn sonar:sonar \
         -Dsonar.projectKey=maven-example-jaquar \
         -Dsonar.organization=manikandance \
         -Dsonar.host.url=https://sonarcloud.io \
         -Dsonar.login=640b58279bec2b519af64c9fdc358b7eff9333a5'  
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

pipeline{
 agent none
 stages{
  stage('build'){
   agent {
    docker {
      image 'maven:3.9.6-eclipse-temurin-17-alpine'
    }
   }
   steps{
    echo 'compile maven app'
    sh 'mvn compile'
   }
  }
 }
}

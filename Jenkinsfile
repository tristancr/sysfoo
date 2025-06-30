pipeline {
    agent any
    tools {
        maven 'Maven 3.9.9'
    }
    stages {
        stage("build") {
            echo 'build'
            sh 'mvn compile'
        }
        stage("test") {
            echo 'test'
            sh 'mvn clean test'
        }
        stage("package") {
            echo 'package'
            sh 'mvn package -DskipTests'
            archiveArtifacts artifacts: '**/target/*.jar', followSymlinks: false
        }
    }
    post {
        always {
            echo 'pipeline terminated'
        }
    }
}

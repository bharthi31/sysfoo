pipeline {
  agent {
    docker {
      image 'maven:3.6.3-jdk-11-slim'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'Compiling sysfoo'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'Testing sysfoo'
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        echo 'Packaging sysfoo'
        sh 'mvn package -DskipTests'
        archiveArtifacts 'target/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
  post {
    always {
      echo 'This pipeline is completed..'
    }

  }
}
pipeline {
  agent any
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

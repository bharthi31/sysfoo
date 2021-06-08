pipeline {
  agent any
  tools {
    maven 'Maven 3.6.3'
  }
  stages{
      stage("Build"){
          steps{
              echo 'Compiling sysfoo'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'Testing sysfoo'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'Packaging sysfoo'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}

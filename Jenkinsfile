pipeline {
  agent any

  tools{
    "Maven 3.6.3"
  }
  
  stages{
      stage("build"){
          steps{
              echo 'compiling sysfoo app..'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'test maven app'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'packaging the sysfoo app...'
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

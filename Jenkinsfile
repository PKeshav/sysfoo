pipeline {
  agent any
  tool {
    maven 'Maven 3.6.3'
  }
  stages{
      stage("build"){
          steps{
              echo 'compile maven app'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'running unit tests'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'packaging app into a war file'
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

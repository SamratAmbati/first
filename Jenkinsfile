pipeline{
  agent any{
    stages{
      stage('clone'){
        steps{
          git 'https://github.com/SamratAmbati/first.git'
        }
      }
      stage('Build'){
        steps{
          echo 'Building the project...'
          sh 'javac helloworld.java'
        }
      }
      stage('Test'){
        steps{
          echo 'Running tests...'
          sh 'java helloworld'
        }
      }
      stage('Deploy'){
        steps{
          echo 'Deploying the project...'
        }
      }
    }
    post{
      success{
        echo 'pipeline completed succesfully'
      }
      failure{
        echo 'pipeline failed.'
      }
    }
  }
}

pipeline {
  agent any
  libraries {
    lib("SharedLibs")
  }
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${MY_NAME}!"
        echo "Test User Name: ${TEST_USER_USR}"
        echo "Test User Password: ${TEST_USER_PSW}"
        echo "Hello ${MY_NAME}!"
        echo "Hello ${params.Name}!"
      }
    }
    stage('Shared Lib') {
      steps {
         helloWorld("Jenkins")
      } 
    }
  }
  environment {
    MY_NAME = 'Mary'
    TEST_USER = credentials('test-user')
  }
  post {
    aborted {
      echo 'Why didn\'t you push my button?'
      
    }
    
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}

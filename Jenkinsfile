pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${MY_NAME}!"
        echo "Test User Name: ${TEST_USER_USR}"
        echo "Test User Password: ${TEST_USER_PSW}"
        echo "Hello ${MY_NAME}!"
        echo "Hello ${params.Name}!"
        echo "Hello ${params.Name.Description}!"
      }
    }
  }
  environment {
    MY_NAME = 'Mary'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}
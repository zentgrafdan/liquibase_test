pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        bat 'C:\\Tools\\datical_prj\\demobats\\dev1.bat'
        bat 'C:\\Tools\\datical_prj\\demobats\\dev2.bat'
      }
    }
    stage('Good To Test') {
      steps {
        input(message: 'OK to go?', id: '0', ok: 'OK')
      }
    }
    stage('Test') {
      steps {
        bat 'C:\\Tools\\datical_prj\\demobats\\test1.bat'
        bat 'C:\\Tools\\datical_prj\\demobats\\test2.bat'
      }
    }
    stage('Good to Prod') {
      steps {
        input(message: 'OK to promote to Prod', id: '1', ok: 'OK')
      }
    }
    stage('Prod') {
      steps {
        bat 'C:\\Tools\\datical_prj\\demobats\\prod1.bat'
        bat 'C:\\Tools\\datical_prj\\demobats\\prod2.bat'
      }
    }
  }
  environment {
    Dev = 'dev'
    Test = 'test'
    Prod = 'prod'
  }
}
pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        sh '''@echo off
cd /d C:\\Tools\\datical_prj\\demodirs\\dev
copy C:\\Tools\\datical_prj\\liquibase_test\\demodb_changelog4.xml .
copy C:\\Tools\\datical_prj\\liquibase_test\\core_liquibase.xml .

'''
        sh '''@echo off
cd /d C:\\Tools\\datical_prj\\demodirs\\dev
C:\\Tools\\datical_prj\\liquibase-3.6.2-bin\\liquibase --changeLogFile=core_liquibase.xml update'''
      }
    }
  }
  environment {
    Dev = 'dev'
    Test = 'test'
    Prod = 'prod'
  }
}
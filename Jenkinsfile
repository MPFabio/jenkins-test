pipeline {
  agent any
  stages {
    stage('clone') {
      steps {
        sh "rm -rf .git"
        sh "git clone https://github.com/MPFabio/jenkins-test"
      }
    }  
    stage('version') {
      steps {
        sh "python3 --version"
      }
    }
    stage('move') {
      steps {
        sh "cd jenkins-test"
      }
    }
    stage('run') {
      steps {
        sh "python3 main.py"
      }
    }
  }
}

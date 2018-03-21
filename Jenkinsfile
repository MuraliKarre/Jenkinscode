pipeline {
  agent any
  stages {
    stage('Shell Commands') {
      steps {
        sh 'echo Hello World - stage1 step1'
        sh 'echo Hello stage1 step2'
      }
    }
    stage('some commands') {
      steps {
        sh 'echo some commands'
      }
    }
  }
}
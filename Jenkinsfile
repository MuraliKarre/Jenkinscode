pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('Git Repo') {
      agent {
        node {
          label 'MAVEN'
        }
        
      }
      steps {
        git(url: 'https://github.com/cit-latex/t1-student-maven-proj.git', branch: 'master')
      }
    }
    stage('Maven compile') {
      agent {
        node {
          label 'MAVEN'
        }
        
      }
      steps {
        sh 'mvn compile'
      }
    }
    stage('Upload Artifates') {
      steps {
        sh 'mvn deploy'
      }
    }
    stage('Ansibel Deploy') {
      steps {
        sh 'ansible --version'
      }
    }
  }
}
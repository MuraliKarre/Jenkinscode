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
        sh 'mvn compile package'
      }
    }
  }
}
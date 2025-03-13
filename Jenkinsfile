pipeline {
  agent any
  stages {
        stage('Clone Repository') {
          steps {
            checkout([$class: 'GitSCM',
            branches: [[name: '*/main']],
            userRemoteConfigs: [[url: 'https://github.com/neelu369/PES2UG22CS363_Jenkins.git']]])
          }
        }
    
    stage('Build'){
      steps {
        build 'PES2UG22CS363-1'
        sh 'g++ main.cpp -o output'
      }
    }

    stage('Test'){
      steps {
        sh './output' sswf3ewge3    
      }
    }

    stage('Deploy'){
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }   
}

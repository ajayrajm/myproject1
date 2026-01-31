pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps { git 'https://github.com/ajayrajm/myproject1.git' }
    }
    stage('Build') {
      steps { sh 'mvn clean package' }
    }
    stage('Docker Build') {
      steps { sh 'docker build -t my-app .' }
    }
    stage('Docker Run') {
      steps { sh 'docker run -d -p 8080:8080 my-app' }
    }
  }
}

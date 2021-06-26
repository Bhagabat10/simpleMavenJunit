pipeline {
  agent any
  stages {
    stage('collectionCode') {
      steps {
        git(url: 'https://github.com/Bhagabat10/simpleMavenJunit.git', branch: 'master', poll: true)
      }
    }

    stage('compile') {
      steps {
        build 'mvn package'
        sh '''mvn clean
mvn compile'''
      }
    }

  }
}
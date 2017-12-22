pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh './gradlew -Dhttp.proxyHost=192.168.62.4 -Dhttp.proxyPort=3128 -Dhttps.proxyHost=192.168.62.4 -Dhttps.proxyPort=3128 clean build -P env=prod'
      }
    }
    stage('Clean up') {
      steps {
        deleteDir()
      }
    }
  }
}
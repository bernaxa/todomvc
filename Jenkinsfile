pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh './gradlew --debug -Dhttp.proxyHost=192.168.62.4 -Dhttp.proxyPort=3128 -Dhttps.proxyHost=192.168.62.4 -Dhttps.proxyPort=3129 clean build -P env=prod'
      }
    }
    stage('Clean up') {
      steps {
        deleteDir()
      }
    }
  }
}
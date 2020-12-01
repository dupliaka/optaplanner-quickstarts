pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        git(url: 'https://github.com/dupliaka/optaplanner-quickstarts.git', branch: 'development')
      }
    }

    stage('Build') {
      steps {
        tool(name: 'maven', type: 'builder')
        sh 'mvn clean install -PfullProfile '
      }
    }

  }
}
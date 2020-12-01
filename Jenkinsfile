pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        git(url: 'https://github.com/dupliaka/optaplanner-quickstarts.git', branch: 'development')
      }
    }

    stage('Build') {
      agent any
      steps {
        tool(type: 'maven builder', name: 'maven')
        sh 'mvn clean install -PfullProfile'
      }
    }

  }
}
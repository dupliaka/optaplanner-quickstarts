pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Initialize') {
      steps {
        git(url: 'https://github.com/dupliaka/optaplanner-quickstarts.git', branch: 'development')
      }
    }

    stage('Build') {
      steps {
        tool(name: 'maven', type: 'maven builder')
        sh 'mvn clean install -PfullProfile'
      }
    }

  }
}
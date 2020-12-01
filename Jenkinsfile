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
        sh 'mvn clean install -PfullProfile'
      }
    }

  }
}
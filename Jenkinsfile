pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        git(url: 'https://github.com/dupliaka/optaplanner-quickstarts.git', branch: 'development')
        sh 'mvnHome = tool \'maven\''
      }
    }

    stage('Build') {
      agent any
      steps {
        sh '\'${mvnHome}/bin/mvn\' clean install -PfullProfile'
      }
    }

  }
}
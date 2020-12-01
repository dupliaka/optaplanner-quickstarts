pipeline {
  agent any
  def mvnHome
  stages {
    stage('Initialize') {
      steps {
        git(url: 'https://github.com/dupliaka/optaplanner-quickstarts.git', branch: 'development')
        mvnHome = tool 'maven'
      }
    }

    stage('Build') {
      agent any
      steps {
        sh "'${mvnHome}/bin/mvn'  clean install -PfullProfile"
      }
    }

  }
}

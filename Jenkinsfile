pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        git(url: 'git@github.com:dupliaka/optaplanner-quickstarts.git', changelog: true, branch: 'development')
      }
    }

  }
}
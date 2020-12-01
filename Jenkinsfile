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
        sh '/home/adupliak/.sdkman/candidates/maven/3.6.3/bin/mvn clean install -PfullProfile'
      }
    }

  }
}

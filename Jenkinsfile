pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://3.110.79.196:9000 \\
  -Dsonar.token=sqp_d19e182ceb24a3e962b0698ee707329fa1ae42cd'''
      }
    }

  }
}
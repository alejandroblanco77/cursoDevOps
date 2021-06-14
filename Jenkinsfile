pipeline {
  agent any
  stages {
    stage('Say Hello') {
      parallel {
        stage('Say Hello') {
          steps {
            sh 'echo "Hello World"'
          }
        }

        stage('build app') {
          agent {
            docker {
              image 'gradle:jdk11'
            }

          }
          steps {
            sh 'sh /home/alejandro_blanco77/cloudshell_open/jenkins-katas/ci/build-app.sh'
          }
        }

      }
    }

  }
}
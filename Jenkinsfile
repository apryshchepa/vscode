pipeline {
  agent none
  stages {
        stage('build') {
            steps {
                echo 'Building with yarn'
                sh 'yarn'
            }
        }
        stage('unit tests') {
            steps {
                sh './scripts/test.sh'
            }
        }
        stage('create windows binaries') {
            steps {
                sh 'yarn run gulp vscode-win32-x64'
            }
        }
  }
}
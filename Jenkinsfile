pipeline {
    agent any
        stages {
        stage('checkout') {
            steps {
                sh 'rm -rf hello-world-war'
                sh 'git clone https://github.com/lalithav23/hello-world-war.git'
            }
        }
         stage('build') {
            steps {
                sh 'docker build -t lalithav23/hello-world-war:1.0.1 .'
            }
        }
    }
}

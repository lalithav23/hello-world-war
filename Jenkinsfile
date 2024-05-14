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
                sh "docker build -t lalithav23/hello-world-war:1.0.1 ."
            }
        }
       stage('publish') {
            steps {
                withCredentials([usernamePassword(credentialsId: '2262c034-c7c2-40ef-8fc8-2bd09e3728a5', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]) {
                    sh "docker login -u ${DOCKER_USERNAME} -p ${DOCKER_PASSWORD}"
                    sh "docker push lalithav23/hello-world-war:1.0.1"
                }
            }
        }     
    }
}

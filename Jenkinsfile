properties([
                        parameters([
                            choice(
                                choices: ['package', 'compile' ],
                                name: 'arg'
                            ),
                           
                           
                            string(
                                defaultValue: '', 
                                name: 'version
                                trim: true
                            )
                        ])
                    ])
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
                sh 'mvn clean package'
            }
        }
    }
}



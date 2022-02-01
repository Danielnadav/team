pipeline {
    agent  any
    stages {
        stage('Build') {
            steps {
                sh 'docker -v'
            }
            
        }
        stage('test') {
            when {
                expression {
                    BRANCH == 'master'
                }
            }
            steps {
                sh 'python -v'
                sh 'ls -la'
            }
        }
        stage('deploy') {
            when {
                expression {
                    BRANCH == 'dev'
                }
            steps {
                sh 'python -v'
                sh 'ls -la'
            }
        }

    }
}
}



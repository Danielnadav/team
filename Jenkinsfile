pipeline {
    agent  any
    stages {
        stage('Build') {
            steps {
                echo 'buliding stage'
            }
            
        }
        stage('test') {
            when {
                expression {
                    BRANCH_NAME == 'dev'
                }
            }
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo "The working branch is ${env.GIT_BRANCH}"
            }
        }
        stage(verifay) {
            steps {
                echo "the working workspace is ${env.WORKSPACE}"

            }
        }
}
// condeitions for post
post {
    always {

    }
    success {
        echo 'the build worked'

    }
}
}



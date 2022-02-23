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
                echo "lets test date ${env.TAG_DATE}"
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
        success {

            echo 'the build worked'

        }
        failure {

            echo 'the build failure'

        }
        aborted {

            echo 'the build aborted'

        }
    }
}



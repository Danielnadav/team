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
                echo "the working workspace is ${env.JOB_DISPLAY_URL}"

            }
        }
}
// condeitions for post
    post {
        success {

            echo 'the build worked'
            echo "The build branch is ${env.GIT_BRANCH}"

        }
        failure {

            echo 'the build failure'

        }
        aborted {

            echo 'the build aborted'

        }
    }
}


// pipeline {
//     agent any
//     parameters {
//     //     booleanParam(name: "TEST_BOOLEAN", defaultValue: true, description: "Sample boolean parameter")
//     //     string(name: "TEST_STRING", defaultValue: "ssbostan", trim: true, description: "Sample string parameter")
//     //     text(name: "TEST_TEXT", defaultValue: "Jenkins Pipeline Tutorial", description: "Sample multi-line text parameter")
//     //     password(name: "TEST_PASSWORD", defaultValue: "SECRET", description: "Sample password parameter")
//            choice(name: "TEST", choices: ["production", "staging", "development"], description: "Sample multi-choice parameter")
//     }
//     stages {
//         stage("Build") {
//             steps {
//                 echo "Build stage."
//                 echo "Hello $params.TEST"
//             }
//         }
//         stage("Test") {
//             steps {
//                 echo "Test stage."
//             }
//         }
//         stage("Release") {
//             steps {
//                 echo "Release stage."
//             }
//         }
//     }
// }
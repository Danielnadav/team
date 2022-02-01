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
                echo $BUILD_NUMBER
            }
        }
}
}



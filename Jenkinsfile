pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('DeployToStaging') {
            script {
                if (env.BRANCH_NAME == 'master'){
                    echo "inside the if"
                    steps {
                        echo 'DEPLOY TO STAGING'
                    }
                } else{
                    steps {
                        echo 'FAILED TO STAGING'
                    }
                }
            }
        }
    }
}

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
stage('myStage') {
    steps {
        echo 'within myStage'
        script {
            if (env.BRANCH_NAME == "master") {
                echo 'triggered by myBranch'
            } else {
                echo 'triggered by something else'
            }
        }
    }
}
    }
}

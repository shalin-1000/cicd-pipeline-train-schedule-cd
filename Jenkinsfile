pipeline {
    agent any
    stages {
        stage ('Building the App') {
            steps {
                echo 'App Building'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip', onlyIfSuccessful: true
            }
        }
        stage ("App Build completed") {
            steps {
                echo 'Build Completed'
            }
        }
    }
}

pipeline {
    agent any

    tools {
        gradle 'Gradle'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/chinmayiii/gradle1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'gradle build'
            }
        }
    }

    post {

        success {
            echo 'Build Successful'
        }

        failure {
            echo 'Build Failed'
        }
    }
}

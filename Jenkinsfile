pipeline {
    agent any

    tools {
        jdk 'JDK'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: '*/master', url: 'https://github.com/junaidahmedjaigirdar24882-sketch/MyMavenToGradle.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew clean build'
            }
        }

        stage('Run Application') {
            steps {
                sh './gradlew run'
            }
        }
    }

    post {
        success {
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}

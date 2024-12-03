pipeline {
    agent any
    stages {
        stage('Preparanding...') {
            steps {
                echo 'Preparando el entorno...'
            }
        }
        stage('Clono Repo') {
            steps {
                echo 'Clonando el repositorio...'
                git branch: 'main', url: 'https://github.com/pablonssss/sitioweb1.git'
            }
        }
        stage('Building...') {
            steps {
                echo 'Building proyect...'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completado exitosamente.'
        }
        failure {
            echo 'El Pipeline falló.'
        }
    }
}

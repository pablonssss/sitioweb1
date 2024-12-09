pipeline {
    agent  {
	label 'NodoAnsible'
    }

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
	stage('Ejecutar Playbook de Ansible') {
            steps {
                sh '''
                ansible-playbook -i /home/ubuntu/inventory /home/ubuntu/install_webservers.yml
                 '''
                
            }
        }
    }
    post {
        success {
            echo 'AHORA SI Pipeline completado exitosamente.'
        }
        failure {
            echo 'El Pipeline falló.'
        }
    }
}

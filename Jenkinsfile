pipeline {
    agent any

    stages {
        stage('Instalação das dependencias') {
             steps {
                bat 'npm install'
            }
        }
           

        stage('Execução ds testes'){
            steps {
                bat 'npm test'
            }

        }
            
    }        

}
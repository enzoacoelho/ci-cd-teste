pipeline {
    agent any

    stages {
        stage('Instalação das dependencias') {
             steps {
                echo 'Instalando os pacotes Node...'
                bat 'npm install'
            }
        }
           

        stage('Execução ds testes'){
            steps {
                echo 'Executando os testes...'
                bat 'chcp 65001 && npx cypress run --quiet --reporter spec'
            }

        }
            
    }        

    post {
        success {
            echo 'Build e testes executados com sucesso'
        }

        failure {
            echo 'Falha na execução'
        }
    }

}
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
                bat 'set MOCHA_REPORTER_OPTIONS=useUnicode=false && npx cypress run --reporter spec'
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
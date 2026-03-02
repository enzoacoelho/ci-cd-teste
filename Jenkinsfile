pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    environment {
        JAVA_TOOL_OPTIONS = "-Dfile.encoding=UTF-8"
        LANG = "pt_BR.UTF-8"
    }

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
                bat 'npm test'
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
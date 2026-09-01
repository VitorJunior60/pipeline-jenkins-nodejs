pipeline {
    agent any
    
    stages{
        stage("Install"){
            steps{
                echo "Instalando dependencias..."
                bat "npm install"
            }
        }
        stage("Build"){
            steps{
                echo "Executando o build..."
                bat "npm run build"
            }
        }
        stage("Test"){
            steps{
                echo "Executando os testes..."
                bat "npm test"
            }
        }
    }
    post {
        success{
            echo "Sucesso"
        } 
        failure {
            echo "fracasso"
        }
    }
}
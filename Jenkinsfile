pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git branch: "main", url: 'https://github.com/CooLVasileff/StudentRegistryApp'
            }
        }
        stage('Install Dependencies'){
            steps{
                script{
                        bat 'npm install'
                }
            }
        }
        stage('Start App'){
            steps{
                script{
                    bat 'start /b npm start'
                }
            }
        }
        stage('Run tests'){
            steps{
                script{
                    bat 'npm test'
                }
            }
        }
    }

    post {
        always{
            echo "CI Pipline Completed"
        }
    }
}

pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch:'main', url:'https://github.com/avinashvijayan/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steps{
                bat 'mvn compile'
            }
        }
        stage('Package'){
            steps{
                bat 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                bat 'java -jar /var/lib/jenkins/workspace/petClinicDecarativePipeline/target/*.jar'
            }
        }
        
    }
}

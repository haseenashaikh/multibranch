pipeline{
    agent any
    stages{
        stage('git clone'){
            steps{
                sh'''
                pwd
                rm -rf *
                git clone https://github.com/haseenashaikh/number-project.git
                '''
            }
        }
        stage('maven1'){
            steps{
                sh'''
                cd number-project
                mvn compile
                '''
            }
        }
        stage('maven2'){
            steps{
                sh'''
                cd number-project
                mvn test
                '''
            }
        }
        stage('maven3'){
            steps{
                sh'''
                cd number-project
                mvn clean
                '''
            }
        }
        stage('maven4'){
            steps{
                sh'''
                cd number-project
                mvn install package
                '''
            }
        }
    }
}

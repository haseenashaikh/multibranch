pipeline{
    agent any
    stages{
        stage('git clone'){
            steps{
                sh'''
                pwd
                rm -rf *
                git clone https://github.com/haseenashaikh/multibranch.git
                '''
            }
        }
        stage('maven1'){
            steps{
                sh'''
                cd multibranch
                mvn compile
                '''
            }
        }
        stage('maven2'){
            steps{
                sh'''
                cd multibranch
                mvn test
                '''
            }
        }
        stage('maven3'){
            steps{
                sh'''
                cd multibranch
                mvn clean
                '''
            }
        }
        stage('maven4'){
            steps{
                sh'''
                cd multibranch
                mvn install package
                '''
            }
        }
    }
}

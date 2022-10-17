pipeline{
    agent any
    stages{
        stage('git clone'){
            steps{
                sh'''
                pwd
                rm -rf *
                git clone https://github.com/haseenashaikh/moon.git
                '''
            }
        }
        stage('maven1'){
            steps{
                sh'''
                cd moon
                mvn clean
                '''
            }
        }
        stage('maven2'){
            steps{
                sh'''
                cd moon
                mvn test
                '''
            }
        }
        stage('maven3'){
            steps{
                sh'''
                cd moon
                mvn clean
                '''
            }
        }
        stage('maven4'){
            steps{
                sh'''
                cd moon
                mvn install package
                '''
            }
        }
    }
}

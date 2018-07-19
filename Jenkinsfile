pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
        stage ('Uruchamiamy mavenProject!!!'){
            steps {
                build job: 'mavenProject'
            }
        }
stage ('Uruchamiamy testyv2!!!'){
            steps{
              
          
            

                build job: 'mavenProject2'
            }

        stage ('Uruchamiamy testy!!!'){
            steps{
              
          
            

                build job: 'testy'
            }
            post {
                success {
                    echo 'Code deployed to Production.'
                }

                failure {
                    echo ' Deployment failed.'
                }
            }
        }


    }
}

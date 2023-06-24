pipeline{
    agent any
    environment{
      staging_server='3.110.83.75'
    }

    stages{
        stage('Deploy to remote'){
            steps{
                sh 'scp ${WORKSPACE}/* root@${staging_server}:/var/www/html/proj01/'        
            }
        }
    }
}

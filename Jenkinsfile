pipeline{
    agent any
    environment{
      staging_server='172.31.33.209'
    }

    stages{
        stage('Deploy to remote'){
            steps{
                sh 'scp ${WORKSPACE}/* root@${staging_server}:/var/www/html/proj01/'        
            }
        }
    }
}

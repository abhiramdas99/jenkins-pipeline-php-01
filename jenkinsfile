pipeline{
    agent any
    environment{
      staging_server=''
    }

    stages{
        stage('Deploy to remote'){
            steps{
                sh 'scp ${WORKSPACE}/* root@${staging_server}:/var/www/html/proj01/'        
            }
        }
    }
}

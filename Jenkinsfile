pipeline{
    agent any
    environment{
      staging_server='172.31.33.209'
    }

    stages{
        stage('Deploy to remote'){
            steps{
                sh 'echo "welcome">file1.txt'
                sh 'scp file1.txt root@${staging_server}:/tmp/'        
            }
        }
    }
}

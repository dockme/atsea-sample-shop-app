// Test
node {
       
       stage('Checkout'){

          checkout scm
       }       
       stage('Build Docker'){

            sh 'cat ./app/Dockerfile'
       }
        
       stage('Deploy'){

         echo 'Push to Repo'

         echo 'ssh to web server and tell it to pull new image'

       }        
}

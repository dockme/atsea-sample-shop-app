// Test
node {
       
       stage('Checkout') {
          checkout scm
       }

       stage('Build Docker alone') {
            docker.build('eu.gcr.io/dockme-666/atseaapp', '-f app/Dockerfile .')
       }
       
       stage('Push') {
            echo $MY_CREDENTIALS
            docker.withRegistry('https://eu.gcr.io/','gcr:dockme-666') { 
                   docker.image('atseaapp').push('latest') 
            }
       }
       
}

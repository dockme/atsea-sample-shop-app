// Test
node {
       
       stage('Checkout') {
          checkout scm
       }
       
       stage('Push') {
            docker.withRegistry('https://eu.gcr.io/','demo-dockme-a8051104f0d8.json') { 
                   docker.build('eu.gcr.io/dockme-666/atseaapp', '-f app/Dockerfile .')
                   docker.image('atseaapp').push('latest') 
            }
       }
       
       stage('Build Docker alone') {
       }

}

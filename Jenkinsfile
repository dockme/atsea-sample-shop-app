// Test
node {
       
       stage('Checkout') {
          checkout scm
       }
       
       stage('Push') {
            docker.withRegistry('https://eu.gcr.io/','dockme-666') { 
                   docker.build('eu.gcr.io/dockme-666/atseaapp', '-f app/Dockerfile .')
                   docker.image('atseaapp').push('latest') 
            }
       }
       
       stage('Build Docker alone') {
       }

}

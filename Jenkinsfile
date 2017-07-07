// Test
node {
       
       stage('Checkout')
          checkout scm

       stage('Build Docker alone')
            docker.build('eu.gcr.io/dockme-666/atseaapp', '-f app/Dockerfile .')

       stage('Push')
            docker.withRegistry('https://eu.gcr.io/','dockme-666') { docker.image('atseaapp').push('latest') }       
}

// Test
node {
       
       stage('Checkout'){

          checkout scm
       }       
       stage('Build Docker'){
            guay = "guay233"
            def app = docker.build('eu.gcr.io/dockme-666/atseaapp', '-f app/Dockerfile .')
            docker.withRegistry('https://eu.gcr.io/','dockme-666') {
                   app.push guay
            }
       }
        
}

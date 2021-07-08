node {
    checkout scm
    stage('Deploying Container') {
        docker.withRegistry('https://registry.hub.docker.com', 'raakhi_docker') {

            def customImage = docker.build("raakhi/py-helloworld:${env.BUILD_ID}")

            /* Push the container to the custom Registry */
            customImage.push()
        }
    }

}

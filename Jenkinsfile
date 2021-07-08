node {
    checkout scm

    docker.withRegistry('https://registry.docker.com', 'raakhi_docker') {

        def customImage = docker.build("py-helloworld:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}

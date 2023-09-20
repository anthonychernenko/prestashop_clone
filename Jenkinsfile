pipeline {
    agent any
    triggers {
        githubPush()
    }
    options { skipDefaultCheckout() }
    stages {
        stage('SSH commands') {
            steps {
                sshagent(['aa5564e9-43aa-4be5-b06b-47ef54f1a6ec']) {
                    sh '''
                    ssh core@178.218.66.40 "cd prestashop2 && sudo docker-compose up -d"
                    '''
                }
            }
        }
    }
}

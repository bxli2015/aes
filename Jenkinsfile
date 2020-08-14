pipeline {
    agent {
        docker {
            image 'openroadcloud/flow'
            args  '--mount type=bind,src="/root/OpenRoadOneStepRun",dst=/cloud'
        }
    }
    stages {
        stage('run') {
            steps {
                sh 'ls -alhs /cloud;'
            }
        }
    }
}

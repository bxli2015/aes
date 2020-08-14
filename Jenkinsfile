pipeline {
    agent {
        docker {
            image 'openroadcloud/flow'
            args  '--entrypoint=/bin/bash --mount type=bind,src="/home/bangxiang/tryopenroad/manualrun/flowuuid",dst=/cloud'
        }
    }
    stages {
        stage('run') {
            steps {
                sh './flow.sh'
            }
        }
    }
}

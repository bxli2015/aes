pipeline {
    agent {
        docker {
            image 'openroadcloud/flow'
            args  '--entrypoint=/bin/bash --mount type=bind,src="/home/bangxiang/tryopenroad/manualrun/flowuuid",dst=/cloud openroadcloud/flow'
        }
    }
    stages {
        stage('run') {
            steps {
                sh 'ls -alhs ./flow.sh'
            }
        }
    }
}

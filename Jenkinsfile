pipeline {
    agent {
        docker {
            image 'openroadcloud/flow'
            args  '--mount type=bind,src="/home/bangxiang/tryopenroad/manualrun/flowuuid",dst=/cloud --entrypoint='
        }
    }
    stages {
        stage('run') {
            steps {
                sh '/OpenROAD-flow/flow/flow.sh'
            }
        }
    }
}

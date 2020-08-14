pipeline {
    agent any
    stages {
        stage('run') {
            steps {
                sh 'work=/home/bangxiang/tryopenroad/manualrun; $work/runflow.sh $work/flowuuid'
            }
        }
    }
}

pipeline {
    agent any
    stages {
        stage('run') {
            steps {
                sh 'work=/root/OpenRoadOneStepRun; $work/runflow.sh $work/flowuuid'
            }
        }
    }
}

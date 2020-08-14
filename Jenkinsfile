  pipeline {
      agent {
          docker {
              image 'openroadcloud/flow'
              args  '--entrypoint='
          }
      }
      stages {
          stage('setup_env') {
              steps {
                  sh 'cd /OpenROAD-flow/flow'
                  sh 'source /OpenROAD-flow/setup_env.sh'
              }
          }
          stage('synth') {
              steps {
                  sh 'make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk synth'
              }
          }
          stage('floorplan') {
              steps {
                  sh 'make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk floorplan'
              }
          }
      }
  }


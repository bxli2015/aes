  pipeline {
      agent {
          docker {
              image 'openroadcloud/flow'
              args  '--entrypoint='
          }
      }
      stages {
          stage('synth') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk synth'
              }
          }
          stage('floorplan') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk floorplan'
              }
          }
      }
  }


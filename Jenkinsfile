  pipeline {
      agent {
          docker {
              image 'openroadcloud/flow'
              args  '--entrypoint='
          }
      }
      stages {
          stage('runme') {
              steps {
                  sh 'cd /OpenROAD-flow/flow'
                  sh 'source /OpenROAD-flow/setup_env.sh'
                  sh 'make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk'
              }
          }
      }
  }


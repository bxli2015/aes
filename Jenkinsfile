  pipeline {
      agent {
          docker {
              image 'openroadcloud/flow'
              args  '--entrypoint='
          }
      }
      stages {
          stage('1-synth') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk synth'
              }
          }
          stage('2-floorplan') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk floorplan'
              }
          }
          stage('3-place') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk place'
              }
          }          
          stage('4-cts') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk cts'
              }
          }          
          stage('5-route') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk route'
              }
          }
          stage('6-gds') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; source /OpenROAD-flow/setup_env.sh; make DESIGN_CONFIG=./designs/nangate45/gcd/config.mk finish'
              }
          }
          stage('show-results') {
              steps {
                  sh 'cd /OpenROAD-flow/flow; ls results/nangate45/gcd/ -alhs'
              }
          }         
      }
  }


pipeline {
  agent none
  stages {
    stage('cov_admin_git') {
      parallel {
        stage('cov_admin_git') {
          steps {
            echo 'cov admin git'
          }
        }

        stage('cpd_cmt') {
          steps {
            echo 'cpd cmt'
          }
        }

        stage('cov_matrix') {
          matrix {
                axes {
                    axis {
                        name "RSERVICE_REPO"
                        values "COMMON_ARCH_X86_64", "UTILS_ARCH_X86_64", "LLDPD_ARCH_X86_64", "XPIF_ARCH_X86_64", "BFD_ARCH_X86_64"
                    }
                }
                stages {
                    stage('coverity') {
                        steps {
                            echo $RSERVICE_REPO
                        }
                    }
                }
            }
        }

      }
    }

  }
}

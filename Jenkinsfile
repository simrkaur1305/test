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
          steps {
            echo 'cov matrix'
          }
        }

      }
    }

  }
}
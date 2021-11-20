pipeline{
  agent any
  environment{
      NEW_VERSION = '1.2.0'
  }
  stages{
    stage('build'){
      steps{
        echo 'buliding'
      }
    }
    stage('test'){
      when{
        expression{
           BRANCH_NAME == 'dev'
          }
      }
      steps{
        echo 'testing'
      }
    }
    stage('deploy'){
      steps{
        echo 'deploying'
      }
    }
  }
}
  

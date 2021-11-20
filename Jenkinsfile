pipeline{
  agent any
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
  

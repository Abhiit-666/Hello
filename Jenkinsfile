pipeline{
  agent any
  parameters{
    choice(name:'VERSION',choices:['1.1','1.2','1.3'],description:'')
    booleanParam(name:'executeTest',defaultValue:true,description:'')
  }
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
           params.executeTest
          }
      }
      steps{
        echo 'testing'
      }
    }
    stage('deploy'){
      steps{
        echo 'deploying'
        echo "deploying version ${params.VERSION}"
      }
    }
  }
}
  

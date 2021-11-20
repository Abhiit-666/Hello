def gv
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
    stage('init'){
      steps{
        script{
          gv= load"script.groovy"
        }
    }
    }
    stage('build'){
      steps{
        script{
          gv.buildApp()
        }
      }
    }
    stage('test'){
      when{
        expression{
           params.executeTest
          }
      }
      steps{
        script{
          gv.testApp()
      }
    }
    }
    stage('deploy'){
      steps{
        script{
          gv.deployApp()
        
      }
     }
    }
  }
}
  

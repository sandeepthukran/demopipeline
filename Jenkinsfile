pipeline {
  agent any
  properties([pipelineTriggers([githubPush()])])
  stages{
    stage('clone') {
      steps{
        git branch: 'main', credentialsId: '6b1baf77-393c-4cd1-98f2-d7d98b689caf', url: 'https://github.com/sandeepthukran/demopipeline'
        echo 'clone done'
      }
    }
    stage('build'){
      steps{
        echo 'build success'
      }
    }
    stage('test'){
      steps{
        echo 'test success'
      }
    }
    stage('deploy'){
      steps{
        echo 'deploy success'
      }
    }
  }
}

pipeline {
  agent any
  properties([parameters([choice(choices: 'master'\n 'main'\n 'dev', description: 'choose the build branch', name: 'branchname')]), pipelineTriggers([githubPush()])])
  stages{
    stage('clone') {
      steps{
        git branch: $'{params.branchname}', credentialsId: '6b1baf77-393c-4cd1-98f2-d7d98b689caf', url: 'https://github.com/sandeepthukran/demopipeline'
        echo 'selected the branch ${params.branchname} done'
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

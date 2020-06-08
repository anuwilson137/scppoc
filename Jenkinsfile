#!groovy
@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        deleteDir()
        checkout scm
       // sh "ls"
      //  script{ datas = readYaml (file: 'mta.yaml') }
      //  echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
        setupCommonPipelineEnvironment script:this
      //  setupCommonPipelineEnvironment(script: this)
    }
    stage('build') {
      mtaBuild script: this
    }
 //   stage('deploy') {
        //cloudFoundryDeploy script: this
  //  }
}

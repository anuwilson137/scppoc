#!groovy

node('BuildAgent-001') {
    @Library('piper-lib-os') _
    stage('prepare') {
        deleteDir()
        checkout scm
      //  echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
        setupCommonPipelineEnvironment script:this
        mtaBuild script: this
        echo pwd
        sh "ls"
    }
  //  stage('build') {
  //      mtaBuild script: this
  //  }
}

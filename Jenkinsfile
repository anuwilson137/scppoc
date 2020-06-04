@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }
    stage('build') {
        //mtaBuild script: this
    }
    stage('deploy') {
        //cloudFoundryDeploy script: this
    }
}

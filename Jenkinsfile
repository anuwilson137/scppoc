@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        checkout scm
        script{ datas = readYaml (file: 'mta.yaml') }
    //    setupCommonPipelineEnvironment script:this
    }
    stage('build') {
        mtaBuild script: this
    }
    stage('deploy') {
        //cloudFoundryDeploy script: this
    }
}

@Library('piper-lib-os') _
node() {
    stage('prepare') {
        checkout([$class: 'GitSCM', branches: [[name: "${params.GIT_BRANCH}"]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'SAP-cloud-Poc',url: "$giturl"]]])
        setupCommonPipelineEnvironment script:this
    }
    stage('build') {
        //mtaBuild script: this
    }
    stage('deploy') {
        //cloudFoundryDeploy script: this
    }
}

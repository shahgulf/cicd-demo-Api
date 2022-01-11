pipeline {
    agent any
    stages {
        stage ('Building') {
            steps {
                bat 'mvn clean install -DskipTests'
            }
        }
		stage ('Testing') {
            steps {
                bat 'mvn test'
            }
        }
		stage ('Deploying') {
            steps {
                bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=4.4.0 -Danypoint.username=ShahgulfQureshi -Danypoint.password=Apisero@123456 -Denv=Sandbox -Dappname=Second-CICD-API -Dbusiness=Apisero -DvCore=Micro -Dworkers=1'}
        }
    }
}
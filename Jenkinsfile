pipeline {
    agent
    { node { label 'master' } }
    stages {
        stage('Snyk Test') {
            steps {
                sh 'ls -la'
                #snykSecurity additionalArguments: '--all-projects --remote-repo-url=goof-github-jenkins-pipeline', failOnIssues: false, snykInstallation: 'SnykPlugin', snykTokenId: 'SnykAPI'
                snykSecurity additionalArguments: '--project-name=goof-jenkins-pipeline', failOnIssues: false, snykInstallation: 'SnykPlugin', snykTokenId: 'SnykAPI'
            }
        }
    }
}

pipeline{
options {
        buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
    }
agent any
tool {
maven 'Apache Maven 3.9.2'
}
stages {
stage('code compilation'){
steps{
echo 'code compilation is starting'
sh 'mvn clean compile'
echo 'code compilation is done'
}
}
stage('Code Package') {
            steps {
                echo 'code packing is starting'
                sh 'mvn clean package'
				echo 'code packing is completed'
            }
        }
stage('status') {
            steps {
                echo 'pipeline completed'
            }
        }
}

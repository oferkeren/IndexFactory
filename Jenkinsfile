pipeline {
    agent { slave } 

    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
    stage('sed Line') {
            steps {
                sh '''sed -i \"461s/.*/self.s.topology.cursor(self.s.db.databaseName+".system.profile", { find: 'system.profile', query: {}}, {}).toArray(callback);/"  $WORKSPACE/node_modules/mongodb/lib/admin.js'''
            }
        }     
    }
}

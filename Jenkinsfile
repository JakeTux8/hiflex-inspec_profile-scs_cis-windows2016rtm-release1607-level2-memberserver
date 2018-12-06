node {
   stage('Deploy') {
      // changing to build directory
      sh 'cd /tmp/build'
      sh 'rm -rf *'
      // Getting profile from a GitHub repository
      sh 'git clone https://github.com/JakeTux8/hiflex-inspec_profile-scs_cis-windows2016rtm-release1607-level2-memberserver.git'
      sh 'inspec compliance login https://chef-automate.example.com --user admin --ent="ei" --insecure --dctoken "93a49a4f2482c64126f7b6015e6b0f30284287ee4054ff8807fb63d9cbd1c506"'
      sh 'inspec compliance upload hiflex-inspec_profile-scs_cis-windows2016rtm-release1607-level2s-memberserver'
      sh 'rm -rf /tmp/build/*'
   }
   stage('Results') {
      echo 'Build Complete'
   }
}

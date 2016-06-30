node ('docker && ubuntu') {
  prepareNode()
  git 'https://github.com/amuniz/okhttp.git'
  def maven = tool 'M3'
  sh "${maven}/bin/mvn clean install -DskipTests"
}

def prepareNode() {
  sh 'apt-get -q -y install default-jdk'
  sh 'apt-get -q -y install git'
  sh 'apt-get -q clean -y && rm -rf /var/lib/apt/lists/* && rm -f /var/cache/apt/*.bin'
}

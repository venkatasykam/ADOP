### Step-1: Install docker engine.

   [Dokcer-Installation-Ubuntu](https://github.com/DevOpsBasicSetup/Phase-2/blob/master/Docker/DockerEngine/2.1.Dokcer-Installation-Ubuntu.md)

### Step-2: Install docker-compose.

  [Dokcer-compose-Installation-Ubuntu](https://github.com/DevOpsBasicSetup/Phase-2/blob/master/Docker/DockerCompose/Installation-and-example-1.md)

### Step-3: Install docker-machine.

  [Dokcer-Machine-Installation-Ubuntu](https://github.com/DevOpsBasicSetup/Phase-2/blob/master/Docker/DokcerMachine/Installation-and-example.md)

### Step-4: Install git & AWSCLI

apt-get update -y

apt-get install git -y

apt-get install python-pip -y

apt install awscli -y

git --version

pip --version

python --version

git clone https://github.com/Accenture/adop-docker-compose.git

cd adop-docker-compose

./quickstart.sh -t aws -m ADOP-DEVOPS -c vpc-02389d534cfa38107 -r us-east-2 -z a -u docker-m -p DevOps@123 -a AKIAJZPIKZWDDADDPCZA -s v6Cdz6DxbJ4SBBXUL6+2FiOHInbKgymbelRVZK+W

1. while getopts "t:m:a:s:c:z:r:u:p:h" opt;

2. if [ -z ${MACHINE_TYPE} ]; then

3. # Switch based on the machine type
     case ${MACHINE_TYPE} in 
	 
4. provision_aws

	Validating the parameters
	
	Create  file with parameters
	
	source_aws 
		# ./conf/provider/env.provider.aws.sh is updating with AWS VPC, keypair, instance name etc (the values which we passed)
		# Export the paramters as env variables
		
	Creating a docker host/machine.
	
		Preapting a docker machine command
		
		Running docker-machine command to create a docker host
	
	

5. Running the command on Dokcer mahine: ./adop compose -m "${MACHINE_NAME}" ${CLI_COMPOSE_OPTS} init

6. Running the command on Dokcer mahine: ./adop certbot gen-export-certs "registry.$(docker-machine ip ${MACHINE_NAME}).nip.io" registry

7. Launch the URL to access dashboard(enter the uname and pwd): http://[publicIp]/  ex: http://18.223.172.213/
OutPut:

root@ip-172-31-15-41:~/adop-docker-compose# ./quickstart.sh -t aws -m ADOP-DEVOP                                                                                                                S -c vpc-02389d534cfa38107 -r us-east-2 -z a -u docker-m -p DevOps@123 -a AKIAJZ                                                                                                                PIKZWDDADDPCZA -s v6Cdz6DxbJ4SBBXUL6+2FiOHInbKgymbelRVZK+W

      ###    ########   #######  ########
     ## ##   ##     ## ##     ## ##     ##
    ##   ##  ##     ## ##     ## ##     ##
   ##     ## ##     ## ##     ## ########
   ######### ##     ## ##     ## ##
   ##     ## ##     ## ##     ## ##
   ##     ## ########   #######  ##


*****************************************************
*                  EVALUATION MODE                  *
*****************************************************
* Quickstart is designed to get you up and running  *
* with the DevOps Platform as quickly as possible.  *
* As such it is not a "production" ready deployment *
* and therefore we brand it as "evaluation mode".   *
* In using quickstart you are acknowledging this,   *
* along with the lack of proper security, backups,  *
* patching, and other operational considerations.   *
*****************************************************

Creating a new AWS variables file...
Creating CA: /root/.docker/machine/certs/ca.pem
Creating client certificate: /root/.docker/machine/certs/cert.pem
Running pre-create checks...
Creating machine...
(ADOP-DEVOPS) Launching instance...
Waiting for machine to be running, this may take a few minutes...
Detecting operating system of created instance...
Waiting for SSH to be available...
Detecting the provisioner...
Provisioning with ubuntu(systemd)...
Installing Docker...
Copying certs to the local machine directory...
Copying certs to the remote machine...
Setting Docker configuration on the remote daemon...
Checking connection to Docker...
Docker is up and running!
To see how to connect your Docker Client to the Docker Engine running on this virtual machine, run: docker-machine env ADOP-DEVOPS

          ###    ########   #######  ########
         ## ##   ##     ## ##     ## ##     ##
        ##   ##  ##     ## ##     ## ##     ##
       ##     ## ##     ## ##     ## ########
       ######### ##     ## ##     ## ##
       ##     ## ##     ## ##     ## ##
       ##     ## ########   #######  ##

* Initialising ADOP
Sourcing provider-specific environment files...
Sourcing ./conf/provider/env.provider.aws.sh parameters file...
Creating a new secrets file...
Your user name is docker-m

Your provided password satisfies the strength criteria.
Generating random passwords for Jenkins, Gerrit, SQL and LDAP admin...
Sourcing variables from platform.secrets.sh file...
The version of your secrets file is up to date, moving on...
* Setting up Docker Network
Created Docker network: local_network
* Pulling Docker Images
Sourcing provider-specific environment files...
Sourcing ./conf/provider/env.provider.aws.sh parameters file...
Your secrets file already exists, will not re-create...
Sourcing variables from platform.secrets.sh file...
The version of your secrets file is up to date, moving on...
Pulling elasticsearch ... done
Pulling logstash      ... done
Pulling kibana        ... done

Pulling sensu-server          ... done
Pulling jenkins-slave         ... done
Pulling ldap-ltb              ... done
Pulling ldap                  ... done
Pulling gerrit                ... done
Pulling selenium-hub          ... done
Pulling sensu-client          ... done
Pulling sonar-mysql           ... done
Pulling gerrit-mysql          ... done
Pulling sensu-rabbitmq        ... done
Pulling ldap-phpadmin         ... done
Pulling nexus                 ... done
Pulling jenkins               ... done
Pulling selenium-node-chrome  ... done
Pulling sonar                 ... done
Pulling sensu-uchiwa          ... done
Pulling sensu-api             ... done
Pulling registry              ... done
Pulling selenium-node-firefox ... done
Pulling proxy                 ... done
Pulling sensu-redis           ... done
* Bringing up ADOP...
Sourcing provider-specific environment files...
Sourcing ./conf/provider/env.provider.aws.sh parameters file...
Your secrets file already exists, will not re-create...
Sourcing variables from platform.secrets.sh file...
The version of your secrets file is up to date, moving on...
Creating elasticsearch ... done
Creating kibana        ... done
Creating logstash      ... done

Creating nexus ...
Creating sensu-rabbitmq ...
Creating jenkins               ... done
Creating gerrit-mysql   ...
Creating ldap-phpadmin         ... done
Creating gerrit-mysql          ... done
Creating nexus                 ... done
Creating registry       ...
Creating sensu-client          ... done
Creating sonar          ...
Creating sensu-rabbitmq        ... done
Creating sensu-api             ... done
Creating sensu-server         ...
Creating selenium-hub         ...
Creating selenium-hub          ... done
Creating ldap                 ...
Creating selenium-node-chrome  ... done
Creating selenium-node-firefox ... done
Creating sonar-mysql          ...
Creating sensu-uchiwa          ... done
Creating proxy                 ...
WARNING: Connection pool is full, discarding connection: 18.223.172.213
Creating sensu-server          ... done
Creating gerrit                ... done
WARNING: Connection pool is full, discarding connection: 18.223.172.213
WARNING: Connection pool is full, discarding connection: 18.223.172.213
Creating sonar-mysql           ... done
WARNING: Connection pool is full, discarding connection: 18.223.172.213
Creating proxy                 ... done
WARNING: Connection pool is full, discarding connection: 18.223.172.213
WARNING: Connection pool is full, discarding connection: 18.223.172.213
WARNING: Connection pool is full, discarding connection: 18.223.172.213
* Waiting for the Platform to become available - this can take a few minutes
Jenkins was unavailable, so slept for: 30 secs
Jenkins was unavailable, so slept for: 30 secs
Jenkins was unavailable, so slept for: 30 secs
Jenkins was unavailable, so slept for: 30 secs
Jenkins was unavailable, so slept for: 30 secs
* Loading the Platform
Generating client certificates for TLS-enabled Engine
/root/docker_certs/cert.pem was generated successfully...
/root/docker_certs/ca.pem was generated successfully...
/root/docker_certs/key.pem was generated successfully...
Uploading certificates to Jenkins Slave at: //root/.docker/
* Waiting for Nginx to become available
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs
Nginx was unavailable, so slept for: 5 secs

##########################################################

SUCCESS, your new ADOP instance is ready!

Run these commands in your shell:
  source ./conf/env.provider.sh
  source credentials.generate.sh
  source env.config.sh

You can check if any variables are missing with: ./adop compose config  | grep 'WARNING'

Navigate to http://18.223.172.213 in your browser to use your new DevOps Platform!
Login using the following credentials:
  Username: docker-m
  Password: DevOps@123
Generate new private key and self-signed certificate...
Copying certificates to the registry_certs volume...
Unable to find image 'busybox:latest' locally
latest: Pulling from library/busybox
8c5a7da1afbc: Pulling fs layer
8c5a7da1afbc: Verifying Checksum
8c5a7da1afbc: Download complete
8c5a7da1afbc: Pull complete
Digest: sha256:cb63aa0641a885f54de20f61d152187419e8f6b159ed11a251a09d115fdff9bd
Status: Downloaded newer image for busybox:latest
a0241a3f6f62
Copying certificates to the ADOP Proxy container...
Copying self-signed certificate to the trusted location /etc/docker/certs.d/...
Copying via docker-machine to the ADOP-DEVOPS...
registry_fullchain.pem                                                                                                                                        100% 1846     1.8KB/s   00:00
Enable registry NGINX configuration...
Restart Docker Registry container with applied certificates...
Restart ADOP Proxy container with updated certificates...
Self-Signed certificates has been generated successfully...
root@ip-172-31-15-41:~/adop-docker-compose#




root@ip-172-31-15-41:~/adop-docker-compose# history
    1  sudo apt-get update
    2  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    3  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    4  sudo apt-get update
    5  apt-cache policy docker-ce
    6  sudo apt-get install -y docker-ce
    7  base=https://github.com/docker/machine/releases/download/v0.14.0 &&   curl -L $base/docker-machine-$(uname -s)-$(uname -m) >/tmp/docker-machine &&   sudo install /tmp/docker-machine /usr/local/bin/docker-machine
    8  curl -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
    9  chmod +x /usr/local/bin/docker-compose
   10  docker-compose version
   11  yum update -y
   12  apt-get update -y
   13  apt-get install git -y
   14  git clone https://github.com/Accenture/adop-docker-compose.git
   15  cd adop-docker-compose/
   16  which docker
   17  which docker-composer
   18  which docker-compose
   19  apt-get -y install python-pip
   20  pip --version
   21  python --version
   22  pip install awscli --upgrade --user
   23  aws --version
   24  which aws
   25  clear
   26  aws --version
   27  apt install awscli
   28  aws --version
   29  clear
   30  ls
   31  ./quickstart.sh -t aws -m ADOP-DEVOPS -c vpc-02389d534cfa38107 -r us-east-2 -z a -u docker-m -p DevOps@123 -a AKIAJZPIKZWDDADDPCZA -s v6Cdz6DxbJ4SBBXUL6+2FiOHInbKgymbelRVZK+W
   32  history
root@ip-172-31-15-41:~/adop-docker-compose#

ASBRL-MARIADB
=========

Deploy a single MariaDB node as a Docker container.

Requirements
------------

Need to be Docker engine installed.

Role Variables
--------------

- default_user: 'ubuntu'
- CONTAINER_NAME: "mariadb"
- DOCKER_CPU_PERIOD: 0
- DOCKER_CPU_QUOTA: 0
- DOCKER_MEMORY: 0
- CONTAINER_STATE: 'started'
- VOLUME_STATE: 'present'
- DOCKER_LABELS:
  - tag1: test
- IMAGE: 'mariadb'
- BUILD: '10.3'
- PORT: 3306
- BIND_ADDRESS: 0.0.0.0
- ROOT_PASSWORD: 'Pa$$w0rd'
- SERVER_ID: 1
- MAX_CONNETIONS: 200
#### MYISAM
- KEY_BUFFER_SIZE: '8M'
- QUERY_CACHE_LIMIT: '128K'
- QUERY_CACHE_SIZE: 64M
- QUERY_CACHE_TYPE: 'ON' #ON/OFF/DEMAND
#### INNODB
- INNODB_FILE_PER_TABLE: 1
- INNODB_BUFFER_POOL_INSTANCES: 4 # Use 1 instance per 1GB of InnoDB pool size
- INNODB_BUFFER_POOL_SIZE: '256M' # Use up to 70-80% of RAM
- INNODB_LOG_BUFFER_SIZE: '16M'
- INNODB_LOG_FILE_SIZE: '128M'
#### LOGGING
- LOG_OUTPUT: 'TABLE' #FILE/TABLE
- GENERAL_LOG: 0
- GENERAL_LOG_FILE: ''
- SLOW_QUERY_LOG: 0
- SLOW_QUERY_LOG_FILE: ''
- LONG_QUERY_TIME: 5
- NEW_DATABASE: ''
- NEW_USER: ''
- NEW_PASSWORD: ''
#### SSL CONFIGS
- SSL_CERT:
- SSL_KEY:
- SSL_KEY:

Dependencies
------------

None

Example Playbook
----------------

      - name: Deploy MariaDB
        include_role:
          name: asbrl-mariadb
        vars:
          ROOT_PASSWORD: 'Pa$$W0rd'

License
-------

BSD

Author Information
------------------

Francisco Chantada
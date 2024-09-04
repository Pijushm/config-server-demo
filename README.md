# Externaltization of configuration using spring-cloud-config

## Spring cloud config server configuration
- Enable application as config server by using annotation `@EnableConfigServer`
- use `spring.cloud.config.server.git.uri` to set the uri of the github/svn repo where we will keep the configuration files
- use `spring.cloud.config.server.default-label` to set the branch we will be using to fetch values from

## Spring cloud config client configuration

- use `spring.cloud.config.uri` to set the config server uri
- also use 'spring.config.import' (default uri is http://locahost:8888)
- if we want to auto refresh properties of a particular bean we can use @RefreshScope annotation and use actuator endpoint `/refesh` to
refresh.
  

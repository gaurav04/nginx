# nginx

Run below command to install nginx 

      sudo apt-get install nginx apache2-utils

In elasticsearh.yml add following lines

      http.cors.enabled : true
  
      http.cors.allow-origin : "*"
  
      http.cors.allow-methods : OPTIONS, HEAD, GET, POST, PUT, DELETE
  
      http.cors.allow-headers : X-Requested-With,X-Auth-Token,Content-Type, Content-Length
  
      http.jsonp.enable: true

Now Restart the elasticsearch 

    service elasticsearch restart
    
    
To generate your .htpasswd file, run this command, replacing kibabaadmin with your own username

    $ sudo htpasswd -c /etc/nginx/conf.d/kibana.htpasswd kibanaadmin
    
Now restart the Nginx service:

    sudo service nginx restart


If we want to use HTTPS genrate ssl cetificate using following links 

      http://wazuh-documentation.readthedocs.io/en/latest/ossec_elk_kibana.html#nginx-secure-proxy

# Using managed elasticsearch service with your Rails app

If you're hosting your Rails app on a EC2 instance or a VM, it is recommended that you use a managed service for elasticsearch, redis and all. Running elasticsearch natively in the VM and using `http://localhost:9200` as your elasticsearch endpoint works fine, but you'll need to manage it yourself. The load on the VM's resources will also be high - that is CPU and memory will be taken up by processes of both the Rails app and elasticsearch. You might need to configure Monit to monitor that the elasticsearch service stays up and is restarted even if it fails.

The better option here is to use a managed elasticsearch instance so that you have one less thing to worry about. If you've created an elastic instance in you cloud provider, you can use the elastic endpoint they provide with your application. Normally if you'd give `http://localhost:9200` as the url for elastic, you can replace it with this particular url.

```
https://abcdefg.eastus.azure.elastic-cloud.com:9243
```

If your elastic instance is password protected, you can provide those credentials from within the url itself while configuring the url as an env variable in Rails


```
https://username:password@abcdefg.eastus.azure.elastic-cloud.com:9243
```
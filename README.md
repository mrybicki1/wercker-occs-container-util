# Step wercker-oracle-occs-container-util
Wercker step to manage Oracle Container Cloud Service container.

# Options

- `occs_user` user name for your Oracle Container Cloud Service (Console) account.
- `occs_password` password for your Oracle Container Cloud Service (Console) account.
- `rest_server_url` Oracle Container Cloud Service Console (manager node) public IP address.
- `function` start|stop|restart the container.
- Determine container using one of the following properties. Listed in evaluation order:
	- `deployment_name` find the container based on the name of the deployment.
	- `service_id` find the container based on the name of the service.
	- `docker_image_name` find the container based on the name of the Docker image.
- `debug` log enabled

# Example

	occs-manage-container:
	  steps:
	    # Manage Oracle Container Cloud Service container
	    - peternagy/oracle-occs-container-util:
	        occs_user: $OCCS_USERNAME
	        occs_password: $OCCS_PASSWORD
	        rest_server_url: $OCCS_REST_SERVER_URL
	        function: restart
			deployment_name: javacro17


This will restart the running or stopped container has deployment name: `javacro17` on Oracle Container Cloud Service.

# peternagy/oracle-occs-container-util

## 0.0.1

- Initial version

# License

The Universal Permissive License (UPL), Version 1.0

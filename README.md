# polymolly
A Helm chart for a Kubernetes wordpress cluster asked by polyConseil


# Notes
If deployed on a Minikube on a VM, we can't access the wordpress service (The nodePort of the wordpress deployment) from the internet, One way to solve this is to install nginx and configure it to proxy to the target port from service list like this : 
- sudo vim /etc/nginx/sites-enabled/default
- look for "proxy_pass" and put proxy_pass http://<minikube IP>:<svc port>;
  
  # PS
  There is still some work to do on the secrets, Helm has a way of handling secrets and I can't locate the issue, feel free to correct this.

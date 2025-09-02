Part1:

1- create pod nginx with name my nginx direct from command don't use yaml file >>> (kubectl run mynginx --image=nginx) >> creating and run pod from nginx image

2- create pod nginx with name my nginx command and use Image nginx123  direct from command don't use yaml file >>> ( when run this command >>> kubectl run mynginx --image=nginx123 give me error >> Error from server (AlreadyExists): pods "mynginx" already exists)
3- check the status and why it doesn't work >> ( Because this name is registered for another pod and I cannot create two pods with the same name )
4- I need to know node name - IP - Image Of the POD >> ( using this command kubectl get po -o wide )
5- delete the pod >> ( using this command >> kubectl delete pod mynginx )
6- scale the replicas to 5 without edit in the Yaml file( using this command >>> kubectl scale rs nginx-rs --replicas=5 )
7- Delete any one of the 5 pods and check what happen and explain ( when using this command kubectl delete pod name-of-pod >> the replicas file create new pod to achieve the number of replicas )
11- find out the issue in the below Yaml (don't use AI) >> ( the issue is matchLabele dont match to template labels )
12- find out the issue in the below Yaml (don't use AI) >> ( the letters in k8s senstive ( in this file we using kind:deployment this mistake the correct kind:Deployment ) )

13- find out the issue in the below Yaml (don't use AI) >> ( error: the path "test_4.yaml" does not exist )

14- what's command you use to know what Image name that running the deployment >> ( kubectl describe deployment deployment-1 | grep -i "Image:"
 ) 

16- replace the image to nginx777 with command directly >> ( using this command kubectl set image deployment/httpd-frontend httpd-container=nginx777 )

17- rollback to pervious version >> ( using this command kubectl rollout undo deployment/httpd-frontend )


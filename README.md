# *Kubernates*
- #### link for kubernate installation help https://www.cloudsigma.com/how-to-install-and-use-kubernetes-on-ubuntu-20-04/
## Namespaces in kubernates
- #### List the current namespaces in a cluster using:
![image](https://user-images.githubusercontent.com/103022040/164165865-4ec38472-b717-48c9-ad49-a0dee07eb0f4.png)
- #### Create a new YAML file called my-namespace.yaml 
![image](https://user-images.githubusercontent.com/103022040/164166543-896729fd-9471-4f0f-aa32-8d91bcafb0df.png)
- #### Edit using nano editor with the contents:
![image](https://user-images.githubusercontent.com/103022040/164166759-9d323ba5-2268-4647-be1a-38580a746f19.png)
- #### Run using following command
![image](https://user-images.githubusercontent.com/103022040/164167853-732dfadb-602e-44c8-8b7c-0655a5caa4bc.png)
- #### Can view new created namespace using following command  
![image](https://user-images.githubusercontent.com/103022040/164192640-29401135-3f1e-4cf5-a664-17f7de0da6d8.png)
- #### Another way of creating namespace is as follows:
![image](https://user-images.githubusercontent.com/103022040/164197405-d34015aa-3293-4380-8334-dbeb306582b2.png)
- #### Delete a namespace with following command
![image](https://user-images.githubusercontent.com/103022040/164198254-9f3d421d-75d0-4894-86c1-8e1102cd264b.png)
# *Pods in Kubernates*
- #### They can be simply created with the kubctl run command, where you have a defined image on the Docker registry which we will pull while creating a pod.
![image](https://user-images.githubusercontent.com/103022040/164211433-0671694a-a571-4ecd-8ca0-b1897af59941.png)
- #### This can also be done by creating the yaml file and then running the kubectl create command.
![image](https://user-images.githubusercontent.com/103022040/164212330-eb893c5d-0c5c-4283-87aa-41c8100b38b9.png)
- #### Multi container pods are created using yaml file with the definition of the containers.
![image](https://user-images.githubusercontent.com/103022040/164372860-832ca4c9-2f43-4501-85ea-ff00b3adf670.png)
# *Implementation of storage class and pvc*
- #### Create a storage class using vi editor
![image](https://user-images.githubusercontent.com/103022040/164388426-662ec096-efee-4d76-bae4-c1068c112147.png)
- #### Create a storage class using following command:
![image](https://user-images.githubusercontent.com/103022040/164389170-e58266aa-9695-41f2-99ff-4b4d6e659501.png)
- #### Let’s create a PVC yaml using the above storage class…
![image](https://user-images.githubusercontent.com/103022040/164390652-6e822921-b3f6-4ab3-9552-00884305f8c8.png)
- #### We can create this resource and check for the following outputs:
![image](https://user-images.githubusercontent.com/103022040/164391288-0910caee-8a55-4b02-9d2c-e1dc5fd32a90.png)
- #### show list of all pvc
![image](https://user-images.githubusercontent.com/103022040/164391654-2732d81d-a4f7-4cc6-899c-d30457815150.png)
# *Daemonset*
- ####  describe a DaemonSet in a YAML file. For example, the daemonset.yaml file below describes a DaemonSet that runs the fluentd-elasticsearch Docker image:
![image](https://user-images.githubusercontent.com/103022040/164427716-fb534b18-1bb9-469b-8b84-774af7bb7760.png)
- #### create a Daemonset using following command:
![image](https://user-images.githubusercontent.com/103022040/164426972-9bcac805-d78c-4475-bce5-cd54532b5284.png)
# *Implementation of Configmap and secret application (with DB)*
- #### In configmap example, we will create a simple YAML that contains the data using vi editor
![image](https://user-images.githubusercontent.com/103022040/164449341-a28ba31f-4319-431e-b17c-9eb5f86f4181.png)
- #### Configmap created using the kubectl apply command as shown below.
 ![image](https://user-images.githubusercontent.com/103022040/164450680-939f33fa-f833-4262-a1d1-850dbdd448f0.png)
- #### Use the following command with the appropriate ConfigMap name defined in the metadata section.
![image](https://user-images.githubusercontent.com/103022040/164451376-69b0fa48-ea6d-4eb3-95ae-bb587ee2ffa4.png)
- #### As secrets are defined by type, let’s create a basic-auth type Secret that contains the database username and password using vi editor
![image](https://user-images.githubusercontent.com/103022040/164452150-a972794f-074d-46ef-9806-dbcc7dc930c8.png)
- #### Secret can be created using the kubectl apply command as shown below.
![image](https://user-images.githubusercontent.com/103022040/164452573-628c2f53-f4ef-4f01-8a8b-0360a23a4297.png)
- #### As secrets contain confidential data, the describe command does not expose this secret data even when the user query through the kubectl using the specific secret name.
 ![image](https://user-images.githubusercontent.com/103022040/164453031-dd716740-699f-44b3-90e3-5885e1cbbd30.png)
# *HelmChart*
- #### use the helmcreate command to create a helmchart
![image](https://user-images.githubusercontent.com/103022040/164621651-7f19a3ec-bf35-4787-89f5-c4eb1e1b862e.png)
- #### Let’s deploy an Apache webserver using Helm. As a first step, we need to tell Helm what location to search by adding a Helm repository:
![image](https://user-images.githubusercontent.com/103022040/164623144-eba6f14d-17e6-4014-a19c-ed9ac75fad8a.png)
- #### Let’s install the actual container:
![image](https://user-images.githubusercontent.com/103022040/164624442-ebc09365-1063-43ad-9ee9-0fab36f4b5ee.png)
- #### After a few minutes your deployment is ready. We can check the state of the containers using kubectl:
![image](https://user-images.githubusercontent.com/103022040/164624996-ce1366ef-1d5a-425a-a1d2-b85307d7314b.png)
- #### Helm can show us information about current deployments:
![image](https://user-images.githubusercontent.com/103022040/164625440-43e7d133-524b-43e3-9d14-e14d812b8eaa.png)
- ####  Helm stores deployment information in secrets – here they are:
![image](https://user-images.githubusercontent.com/103022040/164625967-042c241e-d9f7-4485-b63b-40aaaa67e9ae.png)
 - ## *Deply wordpress using helm chart*
 - #### We can install using command as follows:
 ![image](https://user-images.githubusercontent.com/103022040/164627632-e3fae070-b819-4bfe-a506-722d4536608a.png)
# *GitLab*
- #### Installation of GitLab in ubuntu using following command:
![image](https://user-images.githubusercontent.com/103022040/164684402-ccfc831f-05c8-47e9-9406-95c7222ece74.png)


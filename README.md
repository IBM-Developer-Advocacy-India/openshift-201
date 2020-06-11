# The Ultimate Kubernetes with RedHat OpenShift workshop series: Webcast 2

This part of the workshop is divided in 5 sections:

1. Accessing Openshift Cluster for the workshop
2. Getting started on Openshift Platform on IBM Cloud
- Overview of Openshift on IBM Cloud
- Overview of the Openshift console
- Setting up command line tools to access your cluster
3. Working with projects in Openshift
- Create a project on console and delete from CLI
- Create a project from CLI and delete from console
4. Deploy an application to Openshift
- Deploying to Openshift via 'oc' CLI
- Deployment of code in Github repos
- Source to image (S2I) deployment
5. Trigerring an auto build using GitHub webhooks

## 1. Accessing Openshift Cluster for the workshop

For the purpose of this workshop organizers pre-provisioned for attendees free Red Hat OpenShift Clusters. Thanks to that you can try and learn on how to use them.

The specification of these Red Hat OpenShift clusters is the following:

`3 Worker Nodes
Each Worker Node has 4 CPU cores with 16GB Ram
The abbreviated description:
3 x 4 x 16`

Use this URL to claim the clusters: https://os201ws.mybluemix.net/

![cluster](images/url.png)

Enter the Lab Key given by your instructor, as well as the email address associated with your IBM Cloud account.

After you hit submit, you will be given a cluster for the duration of the workshop.

You should be given the result page showing the successful assignment.

![cloud-account](images/cloud.png)

When you sign up / log in to IBM Cloud, from the Dashboard you need to navigate to IBM Org, you can see the option above 'Create Resources tab' beside Docs and Support.

Next, go to the resource list, from the hamburger menu top left to verify your cluster.

![resource](images/resource-list.png)

Congratulations! You obtained a Red Hat OpenShift 4.3 cluster. Now you are ready for Lab 2.

## 2. Getting started on Openshift Platform on IBM Cloud

https://cloud.ibm.com/docs/openshift?topic=openshift-deploy_app#app_cli

![cloud-account](images/installing-oc-cli.gif)

## 3. Working with projects in Openshift

### Create a project on console

![New project from console](images/new-project-console.gif)

Check your access from the cli

![](images/login-check.gif)

`ibmcloud oc cluster ls`

### View project using the CLI

1. To view a list of projects, run:

`$ oc get projects`

2. You can change from the current project to a different project for CLI operations. The specified project is then used in all subsequent operations that manipulate project-scoped content:

`oc project <project_name>`

![](images/login-view-project-on-cli.gif)

### Create a project from CLI

`oc new-project <project_name> \
   --description="<description>" --display-name="<display_name>"`

For example:

`$ oc new-project hello-openshift \
    --description="This is an example project" \
    --display-name="Hello OpenShift"`

![](images/new-project-cli.gif)

### Viewing a project using the web console

1. Navigate to Home → Projects.

2. Select a project to view.

On this page, click the *Workloads* button to see workloads in the project.

![](images/see-project-on-console.gif)

### Delete a project using the console

1. Navigate to Home → Projects.

2. Locate the project that you want to delete from the list of projects.

3. On the far right side of the project listing, select Delete Project from the Options menu.

4. When the Delete Project pane opens, enter the name of the project that you want to delete in the field.

5. Click Delete.

![](images/delete-on-console.gif)

### Delete a project from CLI

Run `oc delete project <project_name>`

![](images/delete-through-cli.gif)

## 4. Deploy an application to Openshift

![](images.deploy-image-from-external-registry.gif)

### View deployed app

![](images/view-running-app.gif)

### Deployment of code in Github repos

![](images/deploy-from-github.gif)

Deployment successful

![](images/example-project-deployed.png)

### Source to image (S2I) deployment

Fork/Clone this example Python repo so that you can edit on the next step https://github.com/sclorg/django-ex

![](images/s2i-webhook.gif)

## 5. Trigerring an auto build using GitHub Webhooks

![](images/s2i-webhook2.gif)

![](images/s2i-webhook3.gif)

More on Webhooks : https://docs.openshift.com/container-platform/4.1/builds/triggering-builds-build-hooks.html

## More resources:

[OpenShift Container Platform 4.3 Documentation](https://docs.openshift.com/container-platform/4.3/welcome/index.html)

[App Mordernization with a NodeJs app](https://github.com/IBM/node-s2i-openshift)

[App Mordernization with a Java app](https://ibm.github.io/openshift-on-ibm-cloud-workshops)

# HTTP Pull-Push Example

This small example shows a simple HTTP Pull (GET) Push (POST) integration built using
the funktion flow model.

## Running

To run this on OpenShift, just run:

```bash
$ oc new-app fabric8/s2i-java:2.0.0~https://github.com/redhat-ipaas/http-pull-push-example.git

--> Found Docker image d26e8e1 (7 weeks old) from Docker Hub for "fabric8/s2i-java:2.0.0"

    Java Applications 
    ----------------- 
    Platform for building and running plain Java applications (fat-jar and flat classpath)

    Tags: builder, java

    * An image stream will be created as "s2i-java:2.0.0" that will track the source image
    * A source build using source code from https://github.com/redhat-ipaas/http-pull-push-example.git will be created
      * The resulting image will be pushed to image stream "http-pull-push-example:latest"
      * Every time "s2i-java:2.0.0" changes a new build will be triggered
    * This image will be deployed in deployment config "http-pull-push-example"
    * Port 8778/tcp will be load balanced by service "http-pull-push-example"
      * Other containers can access this service through the hostname "http-pull-push-example"

--> Creating resources ...
    imagestream "s2i-java" created
    imagestream "http-pull-push-example" created
    buildconfig "http-pull-push-example" created
    deploymentconfig "http-pull-push-example" created
    service "http-pull-push-example" created
--> Success
    Build scheduled, use 'oc logs -f bc/http-pull-push-example' to track its progress.
    Run 'oc status' to view your app.
```

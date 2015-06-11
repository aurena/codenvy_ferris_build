Ferris for Codenvy.com
====================

This is a stable version of Ferris 2.2 for use with the Codenvy.com web based IDE.

The only difference is the app.yaml file has the routes for static files specifically set, as opposed to being dynamically generated.

You will also need to create a custom config file in order to run the app in Codenvy's environment.  Use the following:

FROM codenvy/python27_gae

EXPOSE 8080
ENV CODENVY_APP_PORT_8000_HTTP 8080

VOLUME ["/home/user/app"]
ENV CODENVY_APP_BIND_DIR /home/user/app
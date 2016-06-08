MogoDB and Morphia for Wildfly.

How to setup?
=============

    cd <WILDFLY_DIR>/modules/system/add-ons
    git clone git@github.com:abdollahpour/wildfly-mongodb-module.git

Restart your wildfly and it's done!

How to use it?
==============
Check JBoss/Wildfly documentations. There's couple of ways to active a module per-application or generally.
If you have ear file you can create `src/main/application/META-INF/jboss-deployment-structure.xml` like:

    <?xml version='1.0' encoding='UTF-8'?>
    <jboss-deployment-structure xmlns="urn:jboss:deployment-structure:1.1">
        <sub-deployment name="boilerplate-ejb.jar">
            <dependencies>
                <module name="org.mongodb.morphia" />
            </dependencies>
        </sub-deployment>
    </jboss-deployment-structure>

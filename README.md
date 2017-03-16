# Quota Exhaustion Action example project

This is one of the ForgeRock Community Projects.
For details, see <https://stash.forgerock.org/projects/COM/repos/about-these-projects/browse>.

If you are reading this on GitHub.com, you are viewing an old version of the project.

## Warning
**This code is not supported by ForgeRock and it is your responsibility to verify that the software is suitable and safe for use.**

## About

This example implementation shows how to simply implement a quota exhaustion action.

## How to install this module

* Put the resulting JAR on the OpenAM classpath (WEB-INF/lib).
* Execute the following ssoadm command:
<pre>
$ openam/bin/ssoadm set-attr-choicevals -s iPlanetAMSessionService -t Global -a iplanet-am-session-constraint-handler -u amadmin -f .pass -p -k myKey=org.forgerock.openam.examples.quotaexhaustionaction.SampleQuotaExhaustionAction
</pre>
* Edit the WEB-INF/classes/amSession.properties file and add the following content:
<pre>
myKey=Randomly Destroy Session
</pre>
* Restart OpenAM

## More info

For more information on this example quota exhaustion action check out this blog entry:
http://blogs.forgerock.org/petermajor/2013/01/session-quota-basics/

* * *
Copyright 2013-2017 ForgeRock AS. All Rights Reserved

Use of this code requires a commercial software license with ForgeRock AS.
or with one of its affiliates. All use shall be exclusively subject
to such license between the licensee and ForgeRock AS.

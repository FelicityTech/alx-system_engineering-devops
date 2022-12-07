# Postmortem


## Issue Summary

The companmy's Server go down for 10 minutes on December 4th 2022. The incident occurred between 6:30pm to 6:40pm WAT. GET requests resulted in 500 internal server error and all users were affected. After a minor update to app, a script asccidentally stopped the web server nginx from running.

## Timeline

the issue was detected 6 minutes after deployment(6:36pm WAT) after a customer lodged a complain about being not able to access the the site. after a minor update to the app, a script accidentally stopped the web server nginx from running and this cost some lost from customer end. Nginx was restarted when some ammendment was amde to the the script that cause the problem.

## Root Cause and Resolution
During the deployment,  a script was accidentally run which stopped the nginx server. The script was found and removed. The nginx server was restarted again and the error was resolved amicably.

## Corrective and Preventative Measures

The develops team had a meeting and agreed that after each deployment, the status of the server should be checked to prevent the same event in the nearest future.

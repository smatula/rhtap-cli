# ACS Scanner

This chart does not deploy any resources, and waits on the initialization of the vulnerability database.

The initialization started when `rhtap-acs` was deployed.
Since it can take upward of 30m for the scanner to be ready, splitting this check in its own chart and running it at the end of the deployment cuts down on deployment time by allowing the install of the other products in parallel.
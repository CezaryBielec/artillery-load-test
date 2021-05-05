In order to run test:

1. Copy the repository
2. In the root of the project run command "npm i"
3. Run command "npm run test-report" to run the test which after completion will generate a report in json format
4. Run command "npm run report" to generate an html report from previously created json report

The test consists of sending a requests to amazon.
It runs for 15 seconds and after each second additional 67 virtual users are sending requests. The cap is set to 1000 virtual users for this one phase.

This test didn't have an impact on this application response time because amazon is prepared for this amount of users, however while i was trying to set up this test on some niche testing blog, i was getting 504 after several dozen requests.

It is also important to keep in mind that load tests should be executed on specifically prepared environment (both hardware and internet conditions).

As far as I'm aware, modern web applications should load at maximum 3 seconds.
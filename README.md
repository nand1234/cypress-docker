# cypress-docker

- cypress version 12.11.0

- steps to run on cypress open and run mode for both E2E and Component testing

- run xhost + to "make sure X11 is setup on machine and echo $DISPLAY retrun value :1 or :0"
   https://laptops.eng.uci.edu/engineering-software/using-linux/configure-ubuntu-for-x11-forwarding-on-startup

- run cypress docker container->  docker-compose -f cypress.yml up -d

- run component test ipad -> docker exec precart-components_cypress_1 cypress run --component -b chrome --config-file cypress-ipad.config.js

- run component test for mobile: docker exec precart-components_cypress_1 cypress run --component -b chrome --config-file cypress-mobile.config.js

- run component test for desktop -> docker exec precart-components_cypress_1 cypress run --component -b chrome --config-file cypress.config.js

- run E2E test -> docker exec precart-components_cypress_1 cypress run -b chrome --config baseUrl=http://localhost:8080 "make sure server is running -> npm run serve:production" 

- run single spec file->  docker exec precart-components_cypress_1 cypress run -b chrome --config-file cypress-ipad.config.js --spec <file.cy.js path>

- cypress open -> docker exec precart-components_cypress_1 cypress open -b chrome --config-file cypress-ipad.config.js

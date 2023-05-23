# cypress-docker

- cypress version 12.11.0
- steps to run
- run cypress docker container->  docker-compose -f cypress.yml up -d
- run xhost + to "unable x-host to conect to cypress"
- run component test ipad -> docker exec precart-components_cypress_1 cypress run --component -b chrome --config-file cypress-ipad.config.js
- run component test for mobile: docker exec precart-components_cypress_1 cypress run --component -b chrome --config-file cypress-mobile.config.js
- run component test for desktop -> docker exec precart-components_cypress_1 cypress run --component -b chrome --config-file cypress.config.js
- run E2E test -> docker exec precart-components_cypress_1 cypress run -b chrome --config baseUrl=http://localhost:8080 "make sure server is running -> npm run serve:production" 
- run single spec file->  docker exec precart-components_cypress_1 cypress run -b chrome --config-file cypress-ipad.config.js --spec <file.cy.js path>

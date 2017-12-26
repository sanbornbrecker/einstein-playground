Deploy to SFDX using the button below:

[![Deploy](https://deploy-to-sfdx.com/dist/assets/images/DeployToSFDX.svg)](https://deploy-to-sfdx.com/deploy?template=https://github.com/sanbornbrecker/einstein-playground)

## Einstein Platform Playgroundサンプル


## インストール手順

1. Authenticate with your hub org (if not already done):
    ```
    sfdx force:auth:web:login -d -a myhuborg
    ```

1. Clone the einstein-playground repository:
    ```
    git clone https://github.com/sanbornbrecker/einstein-playground
    cd einstein-playground
    ```

1. Create a scratch org and provide it with an alias (ep1):
    ```
    sfdx force:org:create -s -f config/project-scratch-def.json -a ep1
    ```

1. Push the app to your scratch org:
    ```
    sfdx force:source:push
    ```

1. Assign the EP permission set to the default user:
    ```
    sfdx force:user:permset:assign -n EP
    ```

1. Open the scratch org:
    ```
    sfdx force:org:open
    ```

1. Upload einstein_platform.pem to File menu
    ```

1. Launch Developer Console and edit EinsteinController.apexc
    ```
    einsteinAccountEmail = ‘Your Email Address for Einstein Platform’
    ```

1. Launch Lightning App Builder and edit visionModelId/sentimentModelId/intentModelId
    ```

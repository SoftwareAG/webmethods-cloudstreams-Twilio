# webMethods CloudStreams Provider for Twilio
This project provides a sample webMethods CloudStreams Provider Project for Twilio. The following APIs are available:
* **Send SMS:** Send a new outgoing SMS. https://www.twilio.com/docs/api/rest/sending-messages
* **Get SMS:** This resource represents an individual SMS message. https://www.twilio.com/docs/api/rest/message
* **Get Account:** An Account instance resource represents a single Twilio account. https://www.twilio.com/docs/api/rest/account
* **Make Call:** Make outgoing call to phones, SIP-enabled endpoints and Twilio Client connections. https://www.twilio.com/docs/api/rest/making-calls
* **Get Call:** A Call instance resource represents a connection between a telephone and Twilio. https://www.twilio.com/docs/api/rest/call
 
## Requirements

The project was developed and tested on the following installation:
1. Integration Server 9.12
2. CloudStreams Server 9.12 Fix 3 (Note: Fix 3 is required for this project to run. Prior fix levels are not supported)
3. Software AG Designer 9.12 with Service Development and CloudStreams Development

## Quick start

To install the project on your local development environment follow these steps.

### Prepare CloudStreams connection

1. In Software AG Designer open ```Window > Preferences```.
2. Navigate to ```Software AG > CloudStreams Servers```.
3. Add your local Integration Server. If there is already an entry make sure username and password are correct by clicking the Test button.

### Import CloudStreams Provider Project

1. In Software AG Designer switch to the ```CloudStreams Development``` perspective.
2. Select File > Import and choose ```Software AG > CloudStreams Provider Project```. Click Next.
3. Select the root of this repository as the Root Directory.
4. Select the ```Twilio``` project.
5. Check ```Copy project into workspace```.
6. Click Finish.
7. Expand the newly imported project.
8. Right-click ```com.softwareag.twilio``` and select Deploy.

### Import Integration Server packages
The CloudStreams Provider Project does not contain neccessary doctypes.

1. Copy Twilio.zip and TwilioTests.zip to ```<install_dir>/IntegrationServer/instances/<instance>/replicate/inbound```.
2. Open Integration Server Administration in your browser.
3. Install both packages with ```Install Inbound Releases``` in Package Management.

### Add Twilio Username and Password and activate connection

To access Twilio a username and password is neccessary. Generate your Twilio Trial account here: https://www.twilio.com/.

1. Open Integration Server Administration in your browser.
2. Navigate to ```Solutions > CloudStreams > Providers > Twilio```.
3. Select ```com.softwareag.twilio``` from the Connector List.

You will find one (disabled) connection: wmtwilioTests:connection. You need to modify this connections:
1. Click the Edit button of the connection.
2. Enter your username and password and save the changes.
3. Enable the connection.

### Run tests

1. In Software AG Designer switch to the ```Service Development``` perspective.
2. Expand the ```TwilioTests``` package.
3. Run the ```*Test``` flow services you find in the subsequent directories.
______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
_____________
Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.

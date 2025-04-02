**Splunk License Redirect App**

**Purpose**

This Splunk app redirects Splunk license information for specific pools from the License Master to the License Slave. It enables License Slaves to view their current usage without requiring direct access to the License Master.

**Why is this Needed?**

When a system is assigned as a License Slave for a pool, its license usage information is sent to the License Master, and it is no longer available on the Slave system.

If a License Slave needs to check its current usage, users must log in to the License Master, which is not ideal for security and accessibility reasons. Instead of granting multiple users access to the License Master, this app sends specific pool information back to the original pool systems, allowing them to view their license usage locally.

**Features**

Redirects license usage data from the License Master back to License Slaves.

Ensures that pool-specific information is available on the respective Slaves.

Enhances security by reducing the need for multiple users to access the License Master.

Automates the process of license information retrieval.

**USAGE**

There are two apps in here:
1. License redirector app which needs to be installed on the License Master
2. License-Slave app which needs to be installed on the Slave machine where you want to see the license information 
**Installation**

Download the app from the GitHub repository.

Copy the configuration files to your Splunk environment.

Restart Splunk to apply changes.

**Configuration**

Modify the configuration files to specify the license pools that should receive redirected data.

Ensure that the Splunk instance running this app has the necessary permissions to communicate with the License Master.

Set up scheduled searches or alerts if necessary to monitor license usage.

**Usage**

The app automatically redirects license data to the appropriate Slaves.

Users can view their license consumption without needing access to the License Master.

Logs are available in Splunk for troubleshooting and verification.

**Future Enhancements**

Provide a Splunk dashboard for better visualization of license usage.

Add support for custom alerting based on license usage thresholds.

**License**

This project is licensed under the MIT License.

**Contributions & Issues**

Feel free to submit issues or contribute improvements via GitHub pull requests.

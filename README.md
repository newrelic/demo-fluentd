[![New Relic Experimental header](https://github.com/newrelic/opensource-website/raw/master/src/images/categories/Experimental.png)](https://opensource.newrelic.com/oss-category/#new-relic-experimental)

# demo-fluentd

This repository is intended to be used with the [demo-deployer](https://github.com/newrelic/demo-deployer). This will install Fluentd as a service on a given host.

The deploy script path to install Fluentd on Linux should be `"deploy_script_path": "/deploy/linux/roles"`. At this time, linux CentOS and AWS Linux1 and Linux2 are supported.

In addition, the deploy config should contain an instrumentor definition for the fluentd service using the with the [demo-newrelic-instrumentation](https://github.com/newrelic/demo-newrelic-instrumentation) repository. Please see the documentation on this repository for the proper deploy script path location.


## Contributing
We encourage your contributions to improve [project name]! Keep in mind when you submit your pull request, you'll need to sign the CLA via the click-through using CLA-Assistant. You only have to sign the CLA one time per project.
If you have any questions, or to execute our corporate CLA, required if your contribution is on behalf of a company,  please drop us an email at opensource@newrelic.com.

**A note about vulnerabilities**

As noted in our [security policy](../../security/policy), New Relic is committed to the privacy and security of our customers and their data. We believe that providing coordinated disclosure by security researchers and engaging with the security community are important means to achieve our security goals.

If you believe you have found a security vulnerability in this project or any of New Relic's products or websites, we welcome and greatly appreciate you reporting it to New Relic through [HackerOne](https://hackerone.com/newrelic).

## License
[Project Name] is licensed under the [Apache 2.0](http://apache.org/licenses/LICENSE-2.0.txt) License.
>[If applicable: The [project name] also uses source code from third-party libraries. You can find full details on which libraries are used and the terms under which they are licensed in the third-party notices document.]

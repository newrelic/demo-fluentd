[![New Relic Experimental header](https://github.com/newrelic/opensource-website/raw/master/src/images/categories/Experimental.png)](https://opensource.newrelic.com/oss-category/#new-relic-experimental)

# demo-fluentd

This repository is intended to be used with the [demo-deployer](https://github.com/newrelic/demo-deployer). This will install Fluentd as a service on a given host.

Here is an example for the `demo-deployer` deploy config to define a fluentd service to be installed on 2 hosts:

```json
{

  "services": [
    {
      "id": "fluentd",
      "destinations": ["Host1","Host2"],
      "source_repository": "https://github.com/newrelic/demo-fluentd.git",
      "deploy_script_path": "deploy/linux/roles",
      "port": 9999
    }
  ]

}
```

In addition, the deploy config should contain an instrumentor definition for the fluentd service using the with the [demo-newrelic-instrumentation](https://github.com/newrelic/demo-newrelic-instrumentation) repository. 

Here is an example of newrelic instrumentation to get the logs for 2 services.

```json
{

  "instrumentations": {
    "services": [
      {
        "id": "nr_logging",
        "service_ids": ["service1"],
        "provider": "newrelic",
        "source_repository": "https://github.com/newrelic/demo-newrelic-instrumentation.git",
        "deploy_script_path": "deploy/logging/roles"
      },
      {
        "id": "nr_logging_in_context",
        "service_ids": ["service2"],
        "provider": "newrelic",
        "source_repository": "https://github.com/newrelic/demo-newrelic-instrumentation.git",
        "deploy_script_path": "deploy/logging_in_context/roles"
      }
    ]
  }

}
```

## Requirements

At this time, linux CentOS and AWS Linux1 and Linux2 are supported.

## Contributing
We encourage your contributions to improve `demo-fluentd`! Keep in mind when you submit your pull request, you'll need to sign the CLA via the click-through using CLA-Assistant. You only have to sign the CLA one time per project.
If you have any questions, or to execute our corporate CLA, required if your contribution is on behalf of a company,  please drop us an email at opensource@newrelic.com.

**A note about vulnerabilities**

As noted in our [security policy](../../security/policy), New Relic is committed to the privacy and security of our customers and their data. We believe that providing coordinated disclosure by security researchers and engaging with the security community are important means to achieve our security goals.

If you believe you have found a security vulnerability in this project or any of New Relic's products or websites, we welcome and greatly appreciate you reporting it to New Relic through [HackerOne](https://hackerone.com/newrelic).

## License
`demo-fluentd` is licensed under the [Apache 2.0](http://apache.org/licenses/LICENSE-2.0.txt) License.

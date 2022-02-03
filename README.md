# Plugin test environment

This repository serves as a template for the test configuration used when reviewing plugin submissions.

- For data source plugins, update [datasources.yml](provisioning/datasources/datasources.yml) with the settings for your test environment.
- Replace [dashboard.json](provisioning/dashboards/dashboards/dashboard.json) with the dashboard definition of a dashboard the demonstrates the main features of your data sources and/or panel.

To provision the plugin on start-up, update the following in the docker-compose.yml to `<URL_TO_ZIP>;<PLUGIN_ID>`:

```
https://example.com/myorg-plugin-panel.zip;myorg-plugin-panel
```

Grafana will download and install the plugin from the URL you specified.

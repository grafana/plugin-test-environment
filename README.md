# Plugin test environment

This repository serves as a template for the test configuration used when reviewing plugin submissions.

- For data source plugins, update [datasources.yml](provisioning/datasources/datasources.yml) with the settings for your test environment.
- Replace [dashboard.json](provisioning/dashboards/dashboards/dashboard.json) with the dashboard definition of a dashboard the demonstrates the main features of your data sources and/or panel.

To install the submitted plugin, run the following in your terminal:

```bash
docker-compose exec grafana grafana-cli --pluginUrl=https://github.com/grafana/singlestat-panel/releases/download/v1.0.0/grafana-singlestat-panel-1.0.0.zip plugins install grafana-singlestat-panel
```

where `--pluginUrl` is the path to the submitted plugin, and `grafana-singlestat-panel` is the ID of the plugin.

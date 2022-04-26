# datafusion_cdap_postaction_plugin
Complete project example for creating a Google cloud datafusion (CDAP) Post action plugin. Sourced and adapted from the documentation where there is no quickstart project.

## Post-run Action Plugin
A PostAction plugin runs arbitrary logic after the end of a pipeline run. It can be set to execute based on whether the run completed successfully, if it failed, or in either case.

The difference between a PostAction and an Action that is placed at the end of a pipeline is that a PostAction will always be executed even if the pipeline run fails, while an Action will only be executed if every stage preceding it successfully runs.

In order to implement a Post-run Action plugin, you extend the PostAction class. Only one method is required to be implemented: run()

### Methods
run(): Used to implement the functionality of the plugin.

configurePipeline(): Used to perform any validation on the application configuration that is required by this plugin or to create any datasets if the fieldName for a dataset is not a macro.
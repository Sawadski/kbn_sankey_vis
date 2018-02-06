# Kibana Sankey Diagram Plugin

This is a sankey diagram visType plugin for Kibana 5.5+.

This plugin was developped from <https://github.com/elastic/kibana/pull/4832>.

Here is an example:

![Sankey](sankey_5_5_Screenshot1.PNG)

# Install

```
git clone https://github.com/JuanCarniglia/kbn_sankey_vis.git
cd kbn_sankey_vis/releases/5.5
npm install d3-sankey-plugin
npm run build
cp -R build/kbn_sankey_vis KIBANA_FOLDER_PATH/installedPlugins/
```

** Note that in NTFS file systems, file paths that exceed 260 characters will fail with cp, you have to use ROBOCOPY:

```
robocopy /S build/kbn_sankey_vis KIBANA_FOLDER_PATH/installedPlugins/kbn_sankey_vis
```

** Also note that if npm run build fails, with a rsync.js error, it is likelly that you don't have RSYNC.EXE installed
in your system, and also that you don't have it on your PATH environment variable.

Install it from https://www.itefix.net/cwrsync and run:

```
set PATH=%PATH%;{rsync installation directory}\bin
```

# Uninstall

```
bin/kibana plugin  --remove kbn_sankey_vis
```

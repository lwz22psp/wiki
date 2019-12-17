# TeamCity部署

teamcity

```bash
docker run -it -d --name teamcity-server-instance  \
    -v ~/tool/TeamCity/data:/data/teamcity_server/datadir \
    -v ~/tool/TeamCity/logs:/opt/teamcity/logs  \
    -p 8011:8111 \
    jetbrains/teamcity-server
```

team city agent

```bash
docker run -it -d -e SERVER_URL="ts:8111" --link teamcity-server-instance:ts -v ~/tool/TeamCity/data/teamcity_agent/conf:/data/teamcity_agent/conf   jetbrains/teamcity-agent
```




# What to After Making a Change to This Repo
- Increment the version of the `<finalName>` tag in `pom.xml`. E.g. `jmxtrans-agent-1.2.12.20-Tags` -> `jmxtrans-agent-1.2.12.21-Tags`.
- Run `mvn clean package`.
- Copy the output jar to https://github.com/depop/kafka-connect/tree/master/docker and update the `jmxtrans-agent` version in https://github.com/depop/kafka-connect/blob/master/Dockerfile.
- Copy the output jar to https://github.com/depop/kafka-default-raw-ingest/tree/master/metrics and update `jmxtrans-agent` version in https://github.com/depop/kafka-default-raw-ingest/blob/master/Dockerfile.
- Merge the result to the `support-tag-queries` branch.
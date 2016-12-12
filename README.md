# OneOps Web Site

This is the source code of the OneOps website available at [http://oneops.com](http://oneops.com).

Please feel free to make PRs to improve the site. Read out [contribution](http://oneops.com/developer/contribution/)
and [documentation guidelines](http://oneops.com/developer/contribution/doc-guideline.html) for more information.

## Building

To view and edit the website you can use standard Jekyll

```
jekyll serve
```

Or you can use the Java implementation included here which only requires a JVM be installed:

```
./jekyll.sh
```

This local build allows you to see the rendered site and access it at
[http://localhost:4000](http://localhost:4000).

# Search

The search feature on the site uses the file http://oneops.com/searchmap-es.json. It is generated from all content
via some Liquid code in the source searchmap-es.json. This file has no newline characters in it to make it suitable
for bullk-loading into Elasticsearch via the REST API on the server.

Helper scripts used on the server can be found in the `scripts\elasticsearch` directory. The `updateOneOpsIndex.sh` script
is currently run manually whenever desired. We might run it daily via CRON in the future. For server and access
detail, contact the contributor team.



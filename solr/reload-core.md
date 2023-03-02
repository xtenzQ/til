# Reload core using SolrJ

```Groovy
def request = new CoreAdminRequest()
request.action = CoreAdminParams.CoreAdminAction.RELOAD
request.coreName = "core_name"
// sometimes it's required to specify the path
request.path = "admin/cores"
request.process(server)
```

<hr>

[Return](../../../)

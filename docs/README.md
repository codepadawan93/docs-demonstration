# 1. H1 Test

> An awesome project.

## 1.1. H2 Test

> Note that this is a test

test

### 1.1.1. H3 Test

> Code sample

```js
const heroes = ["batman", "superman", "aquaman"];
const batman = heroes.map(hero => hero === "batman");
```

> XML Sample

```xml
<heroes>
    <hero>
        <name>Batman</name>
    </hero>
    <hero>
        <name>Superman</name>
    </hero>
    <hero>
        <name>Aquaman</name>
    </hero>
</heroes>

```

```json
{
  "heroes": [
    { "name": "batman" },
    { "name": "superman" },
    { "name": "aquaman" }
  ]
}
```
## 1.2. Script to deactivate update sets
```js
var gr = new GlideRecord('sys_update_set');
gr.addQuery('installed_from=https://clstest.service-now.com^sys_created_by=ekovacs^state=complete');
gr.query();
var i = 0;
while(gr.next()){
    i++;
    gr.setWorkflow(false);
    gs.print(i + gr.name.getDisplayValue().toString());
    gr.state = 'ignore';
    gr.update();
}
gs.print(i);
```

## 1.3. Portal stuff

```css
.sfn-class {
  background-color: salmon;
}
```


> In client controller use `$scope.server.get()`

```js
$scope.server
    .get({action: 'update', target: 'somesysid'})
    .then(function(result){
      process(result);
    })
    .catch(function(exception){
      console.log(exception.toString());
    });
```
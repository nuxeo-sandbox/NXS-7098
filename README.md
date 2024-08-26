# demo-actions

This is a [Nuxeo Studio](https://doc.nuxeo.com/n/dqH) Project to be used as a [multi-layer](https://doc.nuxeo.com/n/LVQ) dependency. The code is being stored in GitHub using the [External Source Repository](https://doc.nuxeo.com/n/ZB4) feature.

This project adds a menu entry in the [Administration interface](https://doc.nuxeo.com/userdoc/administration/) and a layout that can contain “demo actions”, which is to say actions that are related to managing the demo instance, not actions that are part of the demo. An example would be a “demo reset” action.

# Configuration

Contribute your content to the `DEMO_ACTIONS` slot. It will be listed on the page under Administration -> Demo Actions. You can use the built-in `da-demo-action` element, which provides a button (label required) and a description:

```HTML
<nuxeo-slot-content name="demoActionOne" slot="DEMO_ACTIONS">
  <template>
    <da-demo-action label=”My Label” description=”My Description” operation="javascript.myopp"></da-demo-action>
  </template>
</nuxeo-slot-content>
```

Generally speaking `da-demo-action` won’t return anything. Its primary use case is to fire operations that don’t have output.

For custom contributions, it’s recommended to surround your contribution with a nuxeo-card, e.g.:

```HTML
<nuxeo-slot-content name="demoActionOne" slot="DEMO_ACTIONS">
  <template>
    <nuxeo-card>
      <!-- Your stuff -->
    </nuxeo-card>
  </template>
</nuxeo-slot-content>
```

Of course you can use your own custom element as well.

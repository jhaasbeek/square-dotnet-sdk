## Catalog Custom Attribute Definition

Contains information defining a custom attribute. Custom attributes are
intended to store additional information about a catalog object or to associate a
catalog object with an entity in another system. Do not use custom attributes
to store any sensitive information (personally identifiable information, card details, etc.).
[Read more about custom attributes](https://developer.squareup.com/docs/catalog-api/add-custom-attributes)

### Structure

`CatalogCustomAttributeDefinition`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`string`](/doc/models/catalog-custom-attribute-definition-type.md) |  | Defines the possible types for a custom attribute. |
| `Name` | `string` |  | The name of this definition for API and seller-facing UI purposes.<br>The name must be unique within the (merchant, application_id) pair. Required.<br>May not be empty and may not exceed 255 characters. Can be modified after creation. |
| `Description` | `string` | Optional | Seller-oriented description of the meaning of this Custom Attribute,<br>any constraints that the seller should observe, etc. May be displayed as a tooltip in Square UIs. |
| `SourceApplication` | [`Models.SourceApplication`](/doc/models/source-application.md) | Optional | Provides information about the application used to generate an inventory<br>change. |
| `AllowedObjectTypes` | [`IList<string>`](/doc/models/catalog-object-type.md) | Optional | The set of Catalog Object Types that this Custom Attribute may be applied to.<br>Currently, only `ITEM` and `ITEM_VARIATION` are allowed.<br>See [CatalogObjectType](#type-catalogobjecttype) for possible values |
| `SellerVisibility` | [`string`](/doc/models/catalog-custom-attribute-definition-seller-visibility.md) | Optional | Defines the visibility of a custom attribute to sellers in Square<br>client applications, Square APIs or in Square UIs (including Square Point<br>of Sale applications and Square Dashboard). |
| `AppVisibility` | [`string`](/doc/models/catalog-custom-attribute-definition-app-visibility.md) | Optional | Defines the visibility of a custom attribute to applications other than their<br>creating application. |
| `StringConfig` | [`Models.CatalogCustomAttributeDefinitionStringConfig`](/doc/models/catalog-custom-attribute-definition-string-config.md) | Optional | Configuration associated with Custom Attribute Definitions of type `STRING`. |
| `SelectionConfig` | [`Models.CatalogCustomAttributeDefinitionSelectionConfig`](/doc/models/catalog-custom-attribute-definition-selection-config.md) | Optional | Configuration associated with `SELECTION`-type custom attribute definitions. |
| `CustomAttributeUsageCount` | `int?` | Optional | __Read-only.__ The number of custom attributes that reference this<br>custom attribute definition. Set by the server in response to a ListCatalog<br>request with `include_counts` set to `true`.  If the actual count is greater<br>than 100, `custom_attribute_usage_count` will be set to `100`. |
| `Key` | `string` | Optional | The name of the desired custom attribute key that can be used to access<br>the custom attribute value on catalog objects. Cannot be modified after the<br>custom attribute definition has been created. |

### Example (as JSON)

```json
{
  "type": "NUMBER",
  "name": "name0",
  "description": null,
  "source_application": null,
  "allowed_object_types": null,
  "seller_visibility": null,
  "app_visibility": null,
  "string_config": null,
  "selection_config": null,
  "custom_attribute_usage_count": null,
  "key": null
}
```

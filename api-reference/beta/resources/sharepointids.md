---
author: spgraph-docs-team
description: "The SharePointIds resource groups the various identifiers for an item stored in a SharePoint site or OneDrive for Business into a single structure."
ms.date: 09/10/2017
title: SharePointIds
ms.localizationpriority: medium
ms.subservice: "sharepoint"
doc_type: resourcePageType
---
# SharePointIds resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **SharePointIds** resource groups the various identifiers for an item stored in a SharePoint site or OneDrive for Business into a single structure.

**Note:** items returned from OneDrive personal will not include a **SharePointIds** facet.

## Properties

| Property         | Type         | Description|
|:-----------------|:-------------|:-------------------------------------------|
| listId           | string       | The unique identifier (guid) for the item's list in SharePoint.|
| listItemId       | string       | An integer identifier for the item within the containing list.|
| listItemUniqueId | string       | The unique identifier (guid) for the item within OneDrive for Business or a SharePoint site.|
| siteId           | string       | The unique identifier (guid) for the item's site collection (SPSite).|
| siteUrl          | string (url) | The SharePoint URL for the site that contains the item.|
| tenantId         | string       | The unique identifier (guid) for the tenancy.|
| webId            | string       | The unique identifier (guid) for the item's site (SPWeb).|

## Relationships
None.

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "listId", "listItemId", "listItemUniqueId", "siteId", "siteUrl", "webId" ],
  "@odata.type": "microsoft.graph.sharepointIds"
}-->

```json
{
    "listId": "string",
    "listItemId": "string",
    "listItemUniqueId": "string",
    "siteId": "string",
    "siteUrl": "url",
    "tenantId": "string",
    "webId": "string"
}
```

## Remarks

For more information about the facets on a **driveItem**, see [**driveItem**](driveitem.md).



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "The SharepointIds facet provides Sharepoint ids associated with an item.",
  "keywords": "item, unique, id, csom, facet",
  "section": "documentation",
  "tocPath": "Facets/SharepointIds",
  "suppressions": []
}
-->



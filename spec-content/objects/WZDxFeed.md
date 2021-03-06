# WZDxFeed Object (GeoJSON FeatureCollection)
The `WZDxFeed` object is the root (highest level) object of a WZDx feed. There is one WZDx feed object per WZDx GeoJSON document. The `WZDxFeed` is an instance of a [GeoJSON FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3) object.

## Properties
Name | Type | Description | Conformance | Notes
--- | --- | --- | --- | ---
`road_event_feed_info` | [RoadEventFeedInfo](/spec-content/objects/RoadEventFeedInfo.md) | Information about the WZDx feed. | Required | This is a WZDx-specific [foreign member](https://tools.ietf.org/html/rfc7946#section-6.1) and is not part of the GeoJSON specification.
`type` | String; `"FeatureCollection"` | The GeoJSON object type. For WZDx, this must be the string `FeatureCollection`. | Required | This is a GeoJSON property.
`features` | Array; \[[RoadEventFeature](/spec-content/objects/RoadEventFeature.md)\] | An array of GeoJSON [Feature](https://tools.ietf.org/html/rfc7946#section-3.2) objects which represent WZDx road events. | Required | 

## Used By
WZDx GeoJSON document (one `WZDxFeed` object per file).

# Send Event to HubSpot

**Author:** Christophe Goasduff  
**Website:** https://tagstream.co.uk/

## Release Notes

### 01/06/2026
- First version of the template released.

## Overview

This template allows you to create a tag that sends a GA4 event to a HubSpot contact using the `user_id` as the unique identifier.

It is primarily designed for HubSpot users on the Free tier, where custom behavioral events are not available.

When triggered, the tag records a GA4 event of your choice and writes the event name to a custom HubSpot contact property called `latestkeyevent`.

## Requirements

The following custom contact property must exist in HubSpot:

| Property Name |
|--------------|
| `latestkeyevent` |

The template will update this property whenever the tag fires.

## Recommended Usage

This template is intended to be used with GA4 Key Events (formerly known as conversions), although it can be used with any GA4 event.

Typical use cases include:

- Account registration
- Lead generation
- Form submissions
- Subscription upgrades
- Other important user actions

## Important Notes

- The HubSpot contact is identified using the GA4 `user_id` value.
- The `latestkeyevent` property is overwritten each time the tag fires.
- Only the most recently sent event name is stored in HubSpot.
- Historical event tracking is not maintained by this template.
- Ensure that the `user_id` sent to GA4 matches the identifier stored against the HubSpot contact.

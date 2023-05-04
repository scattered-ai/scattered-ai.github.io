---
title: "Auction Protocol"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Auction protocol

## Request

```json
{
    "categories": [ "Boots"],
    "domainName": "test-domain.com",
    "requestId": "c0e5377b-1df8-4e2d-a746-79837004dfda",
    "scenarioId": "d1894d14-2e01-4f6c-92e9-9e1ce20d36f5"
}

```

## Response

```json
{
    "requestId": "120488fe-5dbd-48d1-9a1a-ba090f19909d",
    "products": ["29"],
    "winUrl": "http://localhost:6823/win?brid=120488fe-5dbd-48d1-9a1a-ba090f19909d&lid=3f282c7e-430a-4dcc-bfd8-9780adb937ab&prc=0",
    "clickUrl": "http://localhost:6823/click?brid=120488fe-5dbd-48d1-9a1a-ba090f19909d&lid=3f282c7e-430a-4dcc-bfd8-9780adb937ab&prc=1.5"
}
```
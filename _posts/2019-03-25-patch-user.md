---
category: User
urlpath: '/user/:id/'
title: 'PATCH'
type: 'PATCH'

layout: null
---

### Request

#### Header

```Authorization: Token f887e65a51fd169ae5f69fdd9d8a26152fd98385
Content-Type: application/json```

#### Body

```{
	"email": "test@example.com"
}```

* Specify the item to be updated.

### Response

```200 OK```

```{
    "id": 1,
    "email": "test@example.com",
    "isStaff": false,
    "isActive": true,
    "lastLogin": null,
    "expiredAt": null
}```


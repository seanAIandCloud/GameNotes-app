# GameNotes Database Schema

This file contains database design and schema 

## Users Collection

```json
{
  "id": "ObjectID",
  "name": "String",
  "email": "String (unique)",
  "password": "String",
  "createdAt": "Date",
  "updatedAt": "Date"
}

```
## Notes Collection

```json
{
  "id": "ObjectID",
  "userID": "ObjectID (reference to Users)",
  "title": "String",
  "content": "String",
  "tags": ["String"],
  "isPinned": "Boolean",
  "isArchived": "Boolean",
  "priority": "String (urgent, done, normal)",
  "attachments": [
    {
      "fileUrl": "String",
      "fileType": "String",
      "uploadedAt": "Date"
    }
  ],
  "createdAt": "Date",
  "updatedAt": "Date"
}
```

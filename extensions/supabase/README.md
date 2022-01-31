# Supabase

With this Extension, the open-source database [Supabase](https://supabase.io/) can be connected to a Cognigy.AI virtual agent in order to insert and retrieve **data** and **files** from the database or storage.

## Connection

One has to provide the

- **SupabaseURL** and
- **SupabaseKey**

in a Connection in order to authenticate the virtual agent. Please find more information about the authentication here: https://supabase.io/docs/guides/auth

## Nodes

All Flow Nodes follow the API documentation of Supabase:

- Database
    - [Insert](https://supabase.io/docs/reference/javascript/insert)
    - [Select](https://supabase.io/docs/reference/javascript/select)
- Storage
    - [Get Public URL](https://supabase.io/docs/reference/javascript/storage-from-getpublicurl)
    - [List Files](https://supabase.io/docs/reference/javascript/storage-from-list)

## ToDo

- Example row insert struct
- How to troubleshoot
- Error reporting/logging
  - Why isn't invalid table name reported in log
  - Why doesn't debug level write success messages
  - No error checking/reporting on `createClient`
- How to write unit tests for extensions
- How to mock extensions

### Logging

```js
cognigy.api.log('warn', `${me}:WARNING:Object key '${key.substring(0, 10)} ...' starts with root/relative path - These are not meaningful nor recommended for S3 keys`);
```

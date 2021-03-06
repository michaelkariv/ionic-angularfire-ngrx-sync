An Ionic todo app for testing sync between localstorage and firebase using ngrx.

## my-firebase-app-config.ts
Add to src folder.
``` typescript
import {
    FirebaseAppConfig
} from 'angularfire2';

export class MyFirebaseAppConfig {
    static config: FirebaseAppConfig = {
    apiKey: 'xxxxx',
    authDomain: 'xxxxx',
    databaseURL: 'xxxxx',
    storageBucket: 'xxxxxx''
  };
}
```

## Startup - Basic, no sync
```
[AppFirebase] Firebase Disconnect Success
[Todo] Firebase Load Cancel

[AppFirebase] Firebase Connect
[AppFirebase] Firebase Connect Success
[AppFirebase] Firebase Sync
[AppFirebase] Firebase Sync Success

[Todo] Firebase Load
[Todo] Firebase Load Success
```

## Startup - With sync
```
[AppFirebase] Firebase Disconnect Success
[Todo] Firebase Load Cancel

[AppFirebase] Firebase Connect
[AppFirebase] Firebase Connect Success
[AppFirebase] Firebase Sync
[Todo] Firebase Create 
[Todo] Firebase Update
[Todo] Firebase Delete
[AppFirebase] Firebase Sync Success

[Todo] Firebase Load
[Todo] Firebase Load Success
```

## Online create
```
[Todo] Item Create 
[Todo] Firebase Create 
[Todo] Firebase Load Success
```

## Offline create
```
[Todo] Item Create
[Todo] Local Create
[AppFirebase] Create Offline Action 
```

## Online delete
```
[Todo] Item Delete 
[Todo] Firebase Delete 
[Todo] Firebase Load Success
```

## Offline delete
```
[Todo] Item Delete 
[Todo] Local Delete 
[AppFirebase] Create Offline Action 
```

## Online update
```
[Todo] Item Update 
[Todo] Firebase Update 
[Todo] Firebase Load Success
```

## Offline update
```
[Todo] Item Update
[Todo] Local CreateUpdate
[AppFirebase] Create Offline Action 
```

# Arabi.Chat — Migration Workspace

## New project
- Firebase project: `arab-chat-8148c`
- Android package: `com.arabchat.app`
- Realtime Database: `https://arab-chat-8148c-default-rtdb.firebaseio.com/`

## What was actually extracted
The old XAPK was unpacked and the APK contents were preserved under `extracted/complete_unpack/`.
The package contains the Android client, resources, DEX and embedded client-side constants/paths.

## Confirmed old server dependencies
- `www.malaki.chat`
- `storage.malaki.chat`
- `malaki.chat`
- `/login/google_login.php`
- `/login/google_login2.php`
- `/upload/chat/`
- `/upload/news/`
- `/upload/private/`
- `/upload/room/`
- `/upload/upload/`
- `/upload/wall/`
- `/avatar/`
- `/border/`
- `/cover/`
- `/customrank/`
- `/default_images/`
- `/gifts/`
- `/location/`
- `/media_cache/`
- `/rank`
- `/smile`
- `/sounds/`
- `/video/`
- `download.php`

## Important limitation
The APK does NOT contain the old PHP backend or the old server database. Therefore those server-side components cannot be copied verbatim from the APK.

This workspace separates:
1. extracted client material;
2. confirmed old endpoints;
3. the user's new Firebase configuration;
4. a safe starting database-rules file;
5. migration notes.

No old-server database has been invented or copied.

## Next implementation layer
The actual replacement backend must be implemented against the data contract discovered from the original server or reconstructed from the app's observable behavior. Until that contract is known, the database remains locked.

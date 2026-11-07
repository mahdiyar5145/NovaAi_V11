# NovaOrb AI v11

NovaOrb AI is a Persian-friendly Android WebView assistant with a Cloudflare Workers AI backend.

## Version 11 additions
- Per-account local memory notes (opt-in, stored on this device).
- Cloudflare Workers AI model selector with a server-side allowlist.
- Searchable and pinnable local chat history.
- Theme accent and text-size customization.
- JSON export/import backup for chats and Pro settings.
- Safe basic Markdown rendering and code-copy controls.

## Android
The application ID remains `com.novaorb.ai`. Build with `gradle assembleDebug`.

## Cloudflare
Run `npm install`, then `npm run deploy` after logging in to Wrangler and confirming the `AI` binding. The frontend calls `/api/chat`.

## Important
- Memory, accounts, and chats remain local to the device/browser profile; they are not cloud-synced.
- The model selector is limited to the server allowlist. Availability and usage depend on the Cloudflare account.
- A debug APK built with a different signing key cannot update an already-installed APK. Preserve the original signing key to produce an in-place update.

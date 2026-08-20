# TaskMatch Supabase Realtime Test

Technical proof-of-concept for the validated **two-phone TaskMatch realtime messaging flow**.

## What it tests
- Supabase email/password authentication
- Separate Client and Worker accounts
- Shared `Bathroom Leak` task
- Persistent message history
- Supabase Realtime message delivery between two phones without refresh
- Recipient language preference from the recipient profile
- Manual source-language selection so language metadata is not hard-coded by role

## Two-phone test
1. Phone A: sign in as **Client**.
2. Phone B: sign in as **Worker**.
3. Confirm both show **Realtime connected**.
4. Send a unique message from Phone A and confirm it appears on Phone B without refresh.
5. Reply from Phone B and confirm it appears on Phone A.

## Status
**Phase 1 only:** realtime works; Qwen translation is not connected yet.

For Roman Urdu, select **Urdu** as the message language. Script/transliteration is a separate future field.

## Security
This browser POC contains only the Supabase **publishable** client key. Never add a Supabase secret/service-role key, Qwen API key, passwords, signing keys, or other private credentials to a public repository.

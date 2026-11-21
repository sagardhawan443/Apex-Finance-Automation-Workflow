# Zapier Setup Checklist — Apex Finance

## Suggested flow
1. Trigger: Google Drive — New File in Folder (Apex Finance/Campaigns/2026), OR Catch Hook if Canva/export tooling sends a webhook.
2. Optional action: Google Drive — Create/Upload File if the trigger is from a webhook and the file binary/URL is available.
3. Action: Gmail — Send Email.
   - To: your approved team distribution list
   - Subject: `New Apex Finance campaign asset`
   - Body: include campaign name, file name and Google Drive URL.
4. Test with a non-sensitive sample poster.
5. Confirm correct folder, permissions and email delivery.
6. Turn on the Zap only after review.

## Important configuration notes
- Canva integrations and export triggers depend on your account plan and available Zapier connectors. If direct Canva trigger is unavailable, use a Drive folder trigger or a supported webhook.
- Never paste passwords, API keys or private customer data into project files.
- This guide is not evidence of an activated Zap. Connect accounts and authorize each action yourself.

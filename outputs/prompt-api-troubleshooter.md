# Prompt/API Troubleshooter

## 401 invalid x-api-key
Meaning: The API key is missing, fake, expired, or incorrectly set.

Fix:
- Check that `ANTHROPIC_API_KEY` is set.
- Make sure the value is the real secret key, not the key name.
- Do not paste API keys into GitHub or chat.
- Restart terminal or re-export the key if needed.

## 404 model not found
Meaning: The API key works, but the model ID is wrong or unavailable.

Fix:
- Check the current model ID from the provider docs/dashboard.
- Replace outdated model names like `claude-sonnet-4-20250514`.
- Use a confirmed working model like `claude-sonnet-4-6`.

## NameError: response is not defined
Meaning: The API call failed before creating `response`.

Fix:
- Read the error above it first.
- Fix authentication/model/network issue.
- Re-run the request.

## SDK vs Raw HTTP

SDK:
- Cleaner code.
- Gives Python/JS objects.
- Easier for daily use.

Raw HTTP:
- Shows the real API request.
- Requires headers, JSON body, and manual parsing.
- Better for understanding what SDKs hide.

## Safe API Key Practice

Never commit:
- API keys
- `.env` files
- tokens
- passwords

Use environment variables instead.

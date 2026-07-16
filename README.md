# ard-fngin-ci-test

Firmngin OTA CI/CD test sketch (Arduino / ESP32).

## Local setup

1. Copy `keys.h` from **Firmngin dashboard → Devices → your device**.
2. Open `ard-ci-test.ino` in Arduino IDE and flash.

## GitHub Actions setup

Repo → **Settings → Secrets and variables → Actions**

### Secrets

| Name | Value |
|---|---|
| `FIRMNGIN_API_TOKEN` | API token from **Integrations** (scope: Firmware OTA) |
| `FIRMNGIN_KEYS_H` | Full contents of your local `keys.h` file |

### Variables

| Name | Value |
|---|---|
| `FIRMNGIN_DEVICE_SECRET_ID` | Device **Secret ID** from the dashboard (same as `DEVICE_ID` in `keys.h`) |

## Trigger

- Push to `main`, or
- **Actions → Firmngin OTA → Run workflow**

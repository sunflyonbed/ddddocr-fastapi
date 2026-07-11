# DdddOcr FastAPI Home Assistant Add-on

This repository is structured as a Home Assistant add-on repository.

## Install in Home Assistant

1. Open Home Assistant.
2. Go to **Settings** -> **Add-ons** -> **Add-on Store**.
3. Open the menu in the top right and choose **Repositories**.
4. Add this repository URL:

```text
https://github.com/sunflyonbed/ddddocr-fastapi
```

5. Install **DdddOcr FastAPI**.

The add-on exposes the API on port `8000`. After installation, open the web UI from the add-on page or visit:

```text
http://<home-assistant-host>:8000/docs
```

The add-on files live in [`ddddocr_fastapi`](ddddocr_fastapi/).

# Whats-up Mark-down

A way to talk to markdown wikis powered by LLMs


## Requirements

**python**

```
pip install -r requirements.txt
```

**LLM inference service**

This setup uses a cloudflare workers account with [AI workers](https://developers.cloudflare.com/workers-ai/get-started/rest-api/)

In this case, you need to define the following environment variables:
- `API_TOKEN`
- `API_BASE_URL`

## Get started

1. Place the markdown wikis in a folder called `input_dir`
2. Run `python parse_mds.py --input_dir=input_dir/[NAME]` where `[NAME]` is the root directory of the wiki you want to use. This will create a pickle file into a `.wikis_pkl` directory.
3. Run `streamlit run app.py`
# CLOUDFLARE R2 STORAGE INTEGRATION
**Resource:** Cloudflare R2 Storage  
**Prepared for:** Aerosane  
**Date:** 2025-04-05 08:40:38  

## Introduction

Instructions for integrating Cloudflare R2 object storage, enabling persistent storage for research artifacts, large datasets, and backups.

---

## Python Management Script - `r2_manager.py`

```python
#!/usr/bin/env python3
import boto3, os
from dotenv import load_dotenv

load_dotenv()

class R2:
    def __init__(self):
        self.client = boto3.client('s3',
            aws_access_key_id=os.getenv('R2_ACCESS_KEY'),
            aws_secret_access_key=os.getenv('R2_SECRET_KEY'),
            endpoint_url=os.getenv('R2_ENDPOINT'))

    def upload(self, bucket, local, remote):
        self.client.upload_file(local, bucket, remote)

    def download(self, bucket, remote, local):
        self.client.download_file(bucket, remote, local)

    def list(self, bucket):
        for obj in self.client.list_objects_v2(Bucket=bucket).get('Contents', []):
            print(obj['Key'])

if __name__ == "__main__":
    import sys
    r2 = R2()
    cmd, bucket, *args = sys.argv[1:]
    if cmd == "upload":
        r2.upload(bucket, *args)
    elif cmd == "download":
        r2.download(bucket, *args)
    elif cmd == "list":
        r2.list(bucket)
```

## Example Usage

```bash
python r2_manager.py upload research-bucket localfile.txt remotefile.txt
python r2_manager.py download research-bucket remotefile.txt localfile.txt
python r2_manager.py list research-bucket
```
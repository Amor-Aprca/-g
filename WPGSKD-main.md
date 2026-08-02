# 项目导出

- **项目路径**: `D:\Administrator\Downloads\WPGSKD-main`
- **导出时间**: 2026-08-01 23:16:19
- **排除目录**: .git, .idea, .next, .nuxt, .venv, .vscode, __pycache__, binaries, build, devices, dist, env, node_modules, target, venv
- **排除后缀**: .7z, .avi, .db, .dll, .doc, .docx, .dylib, .env, .eot, .exe, .gif, .gz, .ico, .jpeg, .jpg, .lock, .mp3, .mp4, .pdf, .png, .proto, .pyc, .pyo, .rar, .so, .sqlite, .svg, .tar, .ttf, .wav, .webp, .woff, .woff2, .xls, .xlsx, .zip
- **单文件大小上限**: 5000 KB

## 📂 项目目录结构

```
WPGSKD-main/
  LICENSE
  [help].bat
  [install].bat
  [sync.db].bat
  pyproject.toml
  scripts/
    AddKeysToKeyVault.py
    GetVikiManifestFree.py
    MergeKeyStores.py
    ParseClientID.py
    ParseKeybox.py
    ParsePSSH.py
    TOMLtoYAML.py
    UpdateLocalKeyVault.py
    migrate_credentials.py
    ClientIDGen/
      ClientIDGen.py
      config.example.yml
    VMPBlobGen/
      README.md
      VMPBlobGen.py
    WVD/
      JsonWVDtoStructWVD.py
      MakeWVD.py
  wpgskd/
    __init__.py
    constants.py
    wpgskd.py
    wpgskd.yml
    commands/
      click_utils.py
      dl.py
    config/
      __init__.py
      wpgskd.yml
    core/
      __init__.py
      adobepass.py
      atomic_sql.py
      base64.py
      collections.py
      config.py
      console.py
      constants.py
      credential.py
      decryptor.py
      downloader.py
      events.py
      io.py
      muxer.py
      regex.py
      resolver.py
      services.py
      session.py
      sslciphers.py
      subprocess_utils.py
      utilities.py
      vault.py
      vaults.py
      xml.py
      bamsdk/
        __init__.py
        bamsdk.py
        services/
          __init__.py
          account.py
          bamIdentity.py
          content.py
          device.py
          drm.py
          media.py
          session.py
          token.py
      cdm/
        __init__.py
        base.py
        custom_remote_cdm.py
        detect.py
        loader.py
      decryptors/
        __init__.py
        aes.py
        base.py
      drm/
        __init__.py
        base.py
        clearkey.py
        drmtoday.py
        playready.py
        widevine.py
      manifests/
        __init__.py
        dash.py
        hls.py
        ism.py
        m3u8.py
        map_init.py
      tracks/
        __init__.py
        audio.py
        hdgrange.py
        menu.py
        subtitles.py
        title.py
        tracks.py
        video.py
    servicookies/
      BaseService.py
      __init__.py
      example/
        default.txt
        example.py
        example.yml
    utils/
      gen_esn.py
      MSL/
        MSLKeys.py
        MSLObject.py
        MSL_ANDROID.py
        __init__.py
        schemes/
          EntityAuthentication.py
          KeyExchangeRequest.py
          PlayReadyKeyExchangeScheme.py
          UserAuthentication.py
          __init__.py
    vendor/
      __init__.py
      pymp4/
        __init__.py
        cli.py
        exceptions.py
        parser.py
        util.py
        tools/
          __init__.py
```

## 📄 文件具体内容

### `LICENSE`

```
                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
      outstanding shares, or (iii) beneficial ownership of such entity.

      "You" (or "Your") shall mean an individual or Legal Entity
      exercising permissions granted by this License.

      "Source" form shall mean the preferred form for making modifications,
      including but not limited to software source code, documentation
      source, and configuration files.

      "Object" form shall mean any form resulting from mechanical
      transformation or translation of a Source form, including but
      not limited to compiled object code, generated documentation,
      and conversions to other media types.

      "Work" shall mean the work of authorship, whether in Source or
      Object form, made available under the License, as indicated by a
      copyright notice that is included in or attached to the work
      (an example is provided in the Appendix below).

      "Derivative Works" shall mean any work, whether in Source or Object
      form, that is based on (or derived from) the Work and for which the
      editorial revisions, annotations, elaborations, or other modifications
      represent, as a whole, an original work of authorship. For the purposes
      of this License, Derivative Works shall not include works that remain
      separable from, or merely link (or bind by name) to the interfaces of,
      the Work and Derivative Works thereof.

      "Contribution" shall mean any work of authorship, including
      the original version of the Work and any modifications or additions
      to that Work or Derivative Works thereof, that is intentionally
      submitted to Licensor for inclusion in the Work by the copyright owner
      or by an individual or Legal Entity authorized to submit on behalf of
      the copyright owner. For the purposes of this definition, "submitted"
      means any form of electronic, verbal, or written communication sent
      to the Licensor or its representatives, including but not limited to
      communication on electronic mailing lists, source code control systems,
      and issue tracking systems that are managed by, or on behalf of, the
      Licensor for the purpose of discussing and improving the Work, but
      excluding communication that is conspicuously marked or otherwise
      designated in writing by the copyright owner as "Not a Contribution."

      "Contributor" shall mean Licensor and any individual or Legal Entity
      on behalf of whom a Contribution has been received by Licensor and
      subsequently incorporated within the Work.

   2. Grant of Copyright License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      copyright license to reproduce, prepare Derivative Works of,
      publicly display, publicly perform, sublicense, and distribute the
      Work and such Derivative Works in Source or Object form.

   3. Grant of Patent License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      (except as stated in this section) patent license to make, have made,
      use, offer to sell, sell, import, and otherwise transfer the Work,
      where such license applies only to those patent claims licensable
      by such Contributor that are necessarily infringed by their
      Contribution(s) alone or by combination of their Contribution(s)
      with the Work to which such Contribution(s) was submitted. If You
      institute patent litigation against any entity (including a
      cross-claim or counterclaim in a lawsuit) alleging that the Work
      or a Contribution incorporated within the Work constitutes direct
      or contributory patent infringement, then any patent licenses
      granted to You under this License for that Work shall terminate
      as of the date such litigation is filed.

   4. Redistribution. You may reproduce and distribute copies of the
      Work or Derivative Works thereof in any medium, with or without
      modifications, and in Source or Object form, provided that You
      meet the following conditions:

      (a) You must give any other recipients of the Work or
          Derivative Works a copy of this License; and

      (b) You must cause any modified files to carry prominent notices
          stating that You changed the files; and

      (c) You must retain, in the Source form of any Derivative Works
          that You distribute, all copyright, patent, trademark, and
          attribution notices from the Source form of the Work,
          excluding those notices that do not pertain to any part of
          the Derivative Works; and

      (d) If the Work includes a "NOTICE" text file as part of its
          distribution, then any Derivative Works that You distribute must
          include a readable copy of the attribution notices contained
          within such NOTICE file, excluding those notices that do not
          pertain to any part of the Derivative Works, in at least one
          of the following places: within a NOTICE text file distributed
          as part of the Derivative Works; within the Source form or
          documentation, if provided along with the Derivative Works; or,
          within a display generated by the Derivative Works, if and
          wherever such third-party notices normally appear. The contents
          of the NOTICE file are for informational purposes only and
          do not modify the License. You may add Your own attribution
          notices within Derivative Works that You distribute, alongside
          or as an addendum to the NOTICE text from the Work, provided
          that such additional attribution notices cannot be construed
          as modifying the License.

      You may add Your own copyright statement to Your modifications and
      may provide additional or different license terms and conditions
      for use, reproduction, or distribution of Your modifications, or
      for any such Derivative Works as a whole, provided Your use,
      reproduction, and distribution of the Work otherwise complies with
      the conditions stated in this License.

   5. Submission of Contributions. Unless You explicitly state otherwise,
      any Contribution intentionally submitted for inclusion in the Work
      by You to the Licensor shall be under the terms and conditions of
      this License, without any additional terms or conditions.
      Notwithstanding the above, nothing herein shall supersede or modify
      the terms of any separate license agreement you may have executed
      with Licensor regarding such Contributions.

   6. Trademarks. This License does not grant permission to use the trade
      names, trademarks, service marks, or product names of the Licensor,
      except as required for reasonable and customary use in describing the
      origin of the Work and reproducing the content of the NOTICE file.

   7. Disclaimer of Warranty. Unless required by applicable law or
      agreed to in writing, Licensor provides the Work (and each
      Contributor provides its Contributions) on an "AS IS" BASIS,
      WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
      implied, including, without limitation, any warranties or conditions
      of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
      PARTICULAR PURPOSE. You are solely responsible for determining the
      appropriateness of using or redistributing the Work and assume any
      risks associated with Your exercise of permissions under this License.

   8. Limitation of Liability. In no event and under no legal theory,
      whether in tort (including negligence), contract, or otherwise,
      unless required by applicable law (such as deliberate and grossly
      negligent acts) or agreed to in writing, shall any Contributor be
      liable to You for damages, including any direct, indirect, special,
      incidental, or consequential damages of any character arising as a
      result of this License or out of the use or inability to use the
      Work (including but not limited to damages for loss of goodwill,
      work stoppage, computer failure or malfunction, or any and all
      other commercial damages or losses), even if such Contributor
      has been advised of the possibility of such damages.

   9. Accepting Warranty or Additional Liability. While redistributing
      the Work or Derivative Works thereof, You may choose to offer,
      and charge a fee for, acceptance of support, warranty, indemnity,
      or other liability obligations and/or rights consistent with this
      License. However, in accepting such obligations, You may act only
      on Your own behalf and on Your sole responsibility, not on behalf
      of any other Contributor, and only if You agree to indemnify,
      defend, and hold each Contributor harmless for any liability
      incurred by, or claims asserted against, such Contributor by reason
      of your accepting any such warranty or additional liability.

   END OF TERMS AND CONDITIONS

   APPENDIX: How to apply the Apache License to your work.

      To apply the Apache License to your work, attach the following
      boilerplate notice, with the fields enclosed by brackets "[]"
      replaced with your own identifying information. (Don't include
      the brackets!)  The text should be enclosed in the appropriate
      comment syntax for the file format. We also recommend that a
      file or class name and description of purpose be included on the
      same "printed page" as the copyright notice for easier
      identification within third-party archives.

   Copyright [yyyy] [name of copyright owner]

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

### `[help].bat`

```
@echo off
poetry run wp dl -h
pause
```

### `[install].bat`

```
@echo off
python -m pip install poetry
poetry config virtualenvs.in-project true
poetry install
pause
```

### `[sync.db].bat`

```
@echo off
poetry run python scripts/MergeKeyStores.py -i "H:\BDdownload\key_store.db" -o "H:\WPGSKD\wpgskd\key_store.db"
pause
```

### `pyproject.toml`

```toml
[build-system]
requires = ['poetry-core>=1.0.0']
build-backend = 'poetry.core.masonry.api'

[tool.poetry]
name = 'wpgskd'
version = '0.2.0'
description = 'Widevine, PlayReady, AES-128, and ClearKey downloader and decrypter'
authors = ["WPGSKD Contributors"]

[tool.poetry.dependencies]
python = "^3.10"
requests = {extras = ["socks"], version = "2.32.5"}
curl-cffi = "^0.6.0"
httpx = "^0.23.0"
lxml = "^5.3.0"
m3u8 = "^0.9.0"
isodate = "^0.6.1"
tldextract = "^3.1.0"
validators = "^0.18.2"
websocket-client = "^1.1.0"
pycryptodome = "^3.21.0"
pycryptodomex = "^3.4.3"
ecpy = "^1.2.5"
crccheck = "^1.0"
construct = "2.8.8"
protobuf = "^4.25.1"
base58 = "^2.1.1"
appdirs = "^1.4.4"
click = "^8.1.3"
coloredlogs = "^15.0"
rich = "^13.7.1"
pyyaml = "^6.0.1"
ruamel-yaml = "^0.18.10"
jsonpickle = "^2.0.0"
langcodes = {extras = ["data"], version = "^3.4.0"}
tqdm = "^4.67.1"
Unidecode = "^1.2.0"
pymediainfo = "^5.0.3"
defusedxml = "^0.7.1"
pproxy = "^2.7.7"
pysubs2 = "^1.6.1"
pycaption = "^2.1.1"
chardet = "^5.2.0"
ftfy = "^6.3.1"
pywidevine = "^1.8.0"
pyplayready = {git = "https://git.gay/ready-dl/pyplayready.git"}
numpy = "^1.26.0"
xmltodict = "^1.0.4"
beautifulsoup4 = "^4.11.2"
tinycss = "^0.4"
srt = "^3.5.3"

[tool.poetry.group.dev.dependencies]
flake8 = "^3.8.4"
isort = "^5.9.2"
pyinstaller = "^4.4"
ruff = "^0.6.0"
mypy = "^1.10.0"
bandit = "^1.7.9"
pre-commit = "^3.7.0"
pytest = "^8.0.0"
pytest-asyncio = "^0.23.0"
pytest-cov = "^5.0.0"
responses = "^0.25.0"
types-requests = "^2.31.0"
types-PyYAML = "^6.0.0"

[tool.poetry.scripts]
wp = 'wpgskd.wpgskd:main'

[tool.isort]
line_length = 120
classes = ['CTV', 'FPS', 'IO', 'iTunes', 'MP4', 'TVNOW']
extend_skip = ['scripts/pywidevine', 'wpgskd/vendor']

[tool.ruff]
line-length = 120
target-version = "py310"
force-exclude = true

[tool.ruff.lint]
select = ["E4", "E7", "E9", "F", "W", "I", "UP", "B"]
ignore = ["E501"]

[tool.ruff.lint.per-file-ignores]
"scripts/pywidevine/**" = ["ALL"]
"wpgskd/vendor/**" = ["ALL"]
"tests/**" = ["B011"]

[tool.ruff.format]
quote-style = "double"

[tool.mypy]
python_version = "3.10"
ignore_missing_imports = true
follow_imports = "silent"
check_untyped_defs = false
disallow_untyped_defs = false
warn_unused_ignores = true
warn_redundant_casts = true
exclude = [
    "scripts/pywidevine/",
    "wpgskd/vendor/",
]

[tool.bandit]
exclude_dirs = ["tests", "scripts/pywidevine", "wpgskd/vendor"]
skips = [
    "B101",
    "B324",
    "B413",
    "B314",
    "B608",
]

[tool.pytest.ini_options]
testpaths = ["tests"]
asyncio_mode = "auto"
addopts = "-ra --strict-markers"
markers = [
    "unit: fast, mocked tests (default)",
    "slow: tests that may take >10s",
    "live: end-to-end tests against real services (opt-in via --live)",
]
filterwarnings = [
    "ignore::DeprecationWarning",
]
```

### `scripts\AddKeysToKeyVault.py`

```python
#!/usr/bin/env python3

import argparse
import re
import sqlite3
import sys

from wpgskd.utils.AtomicSQL import AtomicSQL

"""
Add keys to key vault. File should have one KID:KEY per-line.
Optionally you can also put `:<title here>` at the end (after `KEY`).
"""

parser = argparse.ArgumentParser(
    "Key Vault DB batch adder/updater",
    description="Simple script to add or update key information to a vinetrimmer key vault db"
)
parser.add_argument(
    "-t", "--table",
    help="table to store keys to. (e.g. amazon, netflix, disneyplus)",
    required=True)
parser.add_argument(
    "-i", "--input",
    help="data used to parse from",
    required=True)
parser.add_argument(
    "-o", "--output",
    help="key store db that will receive keys",
    required=True)
parser.add_argument(
    "-d", "--dry-run",
    help="execute it, but never actually save/commit changes.",
    action="store_true", required=False)
args = parser.parse_args()

output_db = AtomicSQL()
output_db_id = output_db.load(sqlite3.connect(args.output))

# get all keys from input db
add_count = 0
update_count = 0
existed_count = 0

if args.input == "-":
    input_ = sys.stdin.read()
else:
    with open(args.input, encoding="utf-8") as fd:
        input_ = fd.read()

for line in input_.splitlines(keepends=False):
    match = re.search(r"^(?P<kid>[0-9a-fA-F]{32}):(?P<key>[0-9a-fA-F]{32})(:(?P<title>[\w .:-]*))?$", line)
    if not match:
        continue
    kid = match.group("kid").lower()
    key = match.group("key").lower()
    title = match.group("title") or None

    exists = output_db.safe_execute(
        output_db_id,
        lambda db, cursor: cursor.execute(
            f"SELECT title FROM `{args.table}` WHERE `kid`=:kid",
            {"kid": kid}
        )
    ).fetchone()

    if exists:
        if title and not exists[0]:
            update_count += 1
            print(f"Updating {args.table} {kid}: {title}")
            output_db.safe_execute(
                output_db_id,
                lambda db, cursor: cursor.execute(
                    f"UPDATE `{args.table}` SET `title`=:title",
                    {"title": title}
                )
            )
        else:
            existed_count += 1
            print(f"Key {args.table} {kid} already exists in the db with no differences, skipping...")
    else:
        add_count += 1
        print(f"Adding {args.table} {kid} ({title}): {key}")
        output_db.safe_execute(
            output_db_id,
            lambda db, cursor: cursor.execute(
                f"INSERT INTO `{args.table}` (kid, key_, title) VALUES (:kid, :key, :title)",
                {"kid": kid, "key": key, "title": title}
            )
        )

if args.dry_run:
    print("--dry run enabled, have not commited any changes.")
else:
    output_db.commit(output_db_id)

print(
    "Done!\n"
    f"{add_count} added, {update_count} updated in some way, {existed_count} already existed (skipped)"
)
```

### `scripts\GetVikiManifestFree.py`

```python
#!/usr/bin/env python3

import re
import sys

import requests
from Cryptodome.Cipher import AES

# create a session with a user agent
http = requests.Session()
http.headers.update({
    "User-Agent": "Mozilla/5.0 (X11; Linux x86_64; rv:68.0) Gecko/20100101 Firefox/68.0"
})
# get player fragment page
fragment = http.get(sys.argv[1].replace("/videos/", "/player5_fragment/")).text
# get encrypted manifest urls for both hls and dash
encrypted_manifests = {k: bytes.fromhex(re.findall(
    r'<source\s+type="application/' + v + r'"\s+src=".+?/e-stream-url\?stream=(.+?)"',
    fragment
)[0][0]) for k, v in {"hls": "x-mpegURL", "dash": r"dash\+xml"}.items()}

# decrypt all manifest urls in manifests
m = re.search(r"^\s*chabi:\s*'(.+?)'", fragment, re.MULTILINE)
if not m:
    raise ValueError("Unable to get key")
key = m.group(1).encode()

m = re.search(r"^\s*ecta:\s*'(.+?)'", fragment, re.MULTILINE)
if not m:
    raise ValueError("Unable to get key")
iv = m.group(1).encode()

manifests = {k: AES.new(key, AES.MODE_CBC, iv).decrypt(v).decode("utf-8") for k, v in encrypted_manifests.items()}
# print em out
print(manifests)
```

### `scripts\MergeKeyStores.py`

```python
#!/usr/bin/env python3

import argparse
import sqlite3
import os
import sys

# Add path to import AtomicSQL
sys.path.insert(0, os.path.abspath(os.path.join(os.path.dirname(__file__), '..')))
from wpgskd.utils.AtomicSQL import AtomicSQL

"""
Merge multiple Key Store DBs into one.
Correctly handles multi-table structure (one table per service).
"""

parser = argparse.ArgumentParser(
    "Key Store DB merger",
    description="Script to merge one key store db into another"
)
parser.add_argument(
    "-i", "--input",
    help="key store db that will send keys (Source)",
    required=True)
parser.add_argument(
    "-o", "--output",
    help="key store db that will receive keys (Target)",
    required=True)
args = parser.parse_args()

if not os.path.exists(args.input):
    print(f"Input file not found: {args.input}")
    sys.exit(1)

# Ensure output dir exists
os.makedirs(os.path.dirname(os.path.abspath(args.output)), exist_ok=True)

input_db = AtomicSQL()
input_id = input_db.load(sqlite3.connect(args.input))

output_db = AtomicSQL()
output_id = output_db.load(sqlite3.connect(args.output))

# 1. Get all table names from input DB
tables = input_db.safe_execute(
    input_id,
    lambda db, cursor: cursor.execute("SELECT name FROM sqlite_master WHERE type='table' AND name NOT LIKE 'sqlite_%'")
).fetchall()

tables = [t[0] for t in tables]
print(f"Found tables in input DB: {tables}")

total_added = 0
total_updated = 0
total_skipped = 0

for table in tables:
    print(f"\nProcessing table: {table}...")
    
    # 2. Ensure table exists in output DB
    # We copy the schema from input if it doesn't exist in output
    # But standard vault schema is: id, kid, key_, title
    # To support 'type' column in future, we should check input columns
    
    # Get columns from input table
    input_cols_info = input_db.safe_execute(
        input_id,
        lambda db, cursor: cursor.execute(f"PRAGMA table_info(`{table}`)")
    ).fetchall()
    input_cols = [col[1] for col in input_cols_info]
    
    # Check if table exists in output
    out_table_exists = output_db.safe_execute(
        output_id,
        lambda db, cursor: cursor.execute("SELECT count(name) FROM sqlite_master WHERE type='table' AND name=?", [table])
    ).fetchone()[0] == 1
    
    if not out_table_exists:
        print(f"  - Creating table {table} in output DB...")
        # Standard creation from vaults.py, but let's try to be dynamic if we want 'type' support later
        # For now, stick to standard schema to ensure compatibility with wpgskd
        output_db.safe_execute(
            output_id,
            lambda db, cursor: cursor.execute(
                f"""
                CREATE TABLE IF NOT EXISTS `{table}` (
                    "id"        INTEGER NOT NULL UNIQUE,
                    "kid"       TEXT NOT NULL COLLATE NOCASE,
                    "key_"      TEXT NOT NULL COLLATE NOCASE,
                    "title"     TEXT,
                    PRIMARY KEY("id" AUTOINCREMENT),
                    UNIQUE("kid", "key_")
                );
                """
            )
        )
        # If input has 'type' column, we might want to add it? 
        # Let's handle Requirement 2 separately.

    # 3. Fetch all rows from input table
    rows = input_db.safe_execute(
        input_id,
        lambda db, cursor: cursor.execute(f"SELECT kid, key_, title FROM `{table}`")
    ).fetchall()
    
    for kid, key, title in rows:
        # Check existence in output
        exists = output_db.safe_execute(
            output_id,
            lambda db, cursor: cursor.execute(
                f"SELECT title FROM `{table}` WHERE kid=? AND key_=?",
                [kid, key]
            )
        ).fetchone()
        
        if exists:
            # Update title if missing
            current_title = exists[0]
            if title and not current_title:
                output_db.safe_execute(
                    output_id,
                    lambda db, cursor: cursor.execute(
                        f"UPDATE `{table}` SET title=? WHERE kid=? AND key_=?",
                        (title, kid, key)
                    )
                )
                total_updated += 1
                # print(f"    Updated {kid}")
            else:
                total_skipped += 1
        else:
            # Insert
            output_db.safe_execute(
                output_id,
                lambda db, cursor: cursor.execute(
                    f"INSERT INTO `{table}` (kid, key_, title) VALUES (?, ?, ?)",
                    (kid, key, title)
                )
            )
            total_added += 1
            print(f"    Added {kid}")

output_db.commit(output_id)

print("\n" + "="*30)
print(f"Merge Complete!")
print(f"Added:   {total_added}")
print(f"Updated: {total_updated}")
print(f"Skipped: {total_skipped}")
print("="*30)
```

### `scripts\ParseClientID.py`

```python
#!/usr/bin/env python3

import argparse

from pywidevine.device import LocalDevice
from pywidevine.protos.widevine_pb2 import ClientIdentification

parser = argparse.ArgumentParser(
    "Client identification parser",
    description="Simple script to read a client id blob to see information about it"
)
parser.add_argument(
    "input",
    help="client id blob bin path or path to a wvd file",
)
args = parser.parse_args()

client_id = ClientIdentification()
is_wvd = args.input.lower().endswith(".wvd")

with open(args.input, "rb") as fd:
    data = fd.read()

if is_wvd:
    client_id = LocalDevice.load(data).client_id
else:
    client_id.ParseFromString(data)

print(client_id)
```

### `scripts\ParseKeybox.py`

```python
#!/usr/bin/env python3

import argparse

from pywidevine.keybox import Keybox

parser = argparse.ArgumentParser(
    "Keybox parser",
    description="Simple script to read a keybox to see information about it"
)
parser.add_argument(
    "-k", "--keybox",
    help="keybox path",
    required=True)
args = parser.parse_args()

keybox = Keybox.load(args.keybox)
print(repr(keybox))
```

### `scripts\ParsePSSH.py`

```python
#!/usr/bin/env python3

import argparse
import base64

from pywidevine.protos.widevine_pb2 import WidevineCencHeader
from wpgskd.vendor.pymp4.parser import Box

parser = argparse.ArgumentParser(
    "PSSH parser",
    description="Simple script to read a PSSH to see information about it"
)
parser.add_argument(
    "input",
)
args = parser.parse_args()

args.input = base64.b64decode(args.input.encode("utf-8"))
box = Box.parse(args.input)
cenc_header = WidevineCencHeader()
cenc_header.ParseFromString(box.init_data)

print("pssh box:")
print(box)

print("init_data parsed as WidevineCencHeader:")
print(cenc_header)

print("init_data's key_id as hex:")
print(cenc_header.key_id[0].hex())
```

### `scripts\TOMLtoYAML.py`

```python
#!/usr/bin/env python3

import argparse
import json
import os

import toml
import yaml

parser = argparse.ArgumentParser()
parser.add_argument("path", help="directory containing .toml files to convert")
args = parser.parse_args()

for root, dirs, files in os.walk(args.path):
    for f in files:
        if f.endswith(".toml"):
            data = toml.load(os.path.join(root, f))
            # Convert to a real dict instead of weird toml object that pyyaml can't handle
            data = json.loads(json.dumps(data))
            with open(os.path.join(root, f"{os.path.splitext(f)[0]}.yml"), "w") as fd:
                print(f"Writing {os.path.realpath(fd.name)}")
                fd.write(yaml.safe_dump(data, sort_keys=False))
```

### `scripts\UpdateLocalKeyVault.py`

```python
#!/usr/bin/env python3

import argparse
import json
import sqlite3

from wpgskd.utils.AtomicSQL import AtomicSQL


class LocalVault:
    def __init__(self, vault_path):
        """
        Update local key vault to newer system.
        This should ONLY be run if you have the old structure with keys in a table named `keys`.
        It will move and update the structure of the items in `keys` to their respective new locations and structure.
        :param vault_path: sqlite db path
        """
        self.adb = AtomicSQL()
        self.ticket = self.adb.load(sqlite3.connect(vault_path))
        if not self.table_exists("keys"):
            return
        rows = self.adb.safe_execute(
            self.ticket,
            lambda db, cursor: cursor.execute("SELECT `service`, `title`, `content_keys` FROM `keys`")
        ).fetchall()
        for service, title, content_keys in rows:
            service = service.lower()
            content_keys = json.loads(content_keys)
            if not self.table_exists(service):
                self.create_table(service)
            for kid, key in [x.split(":") for x in content_keys]:
                print(f"Inserting: {kid} {key} {title}")
                existing_row, existing_title = self.row_exists(service, kid, key)
                if existing_row:
                    if title and not existing_title:
                        print(" -- exists, but the title doesn't, so ill merge")
                        self.adb.safe_execute(
                            self.ticket,
                            lambda db, cursor: cursor.execute(
                                f"UPDATE `{service}` SET `title`=? WHERE `kid`=? AND `key_`=?",
                                (title, kid, key)
                            )
                        )
                        continue
                    print("  -- skipping (exists already)")
                    continue
                self.adb.safe_execute(
                    self.ticket,
                    lambda db, cursor: cursor.execute(
                        f"INSERT INTO `{service}` (kid, key_, title) VALUES (?, ?, ?)",
                        (kid, key, title)
                    )
                )
        self.adb.commit(self.ticket)

    def row_exists(self, table, kid, key):
        return self.adb.safe_execute(
            self.ticket,
            lambda db, cursor: cursor.execute(
                f"SELECT count(id), title FROM `{table}` WHERE kid=? AND key_=?",
                [kid, key]
            )
        ).fetchone()

    def table_exists(self, name):
        return self.adb.safe_execute(
            self.ticket,
            lambda db, cursor: cursor.execute(
                "SELECT count(name) FROM sqlite_master WHERE type='table' AND name=?",
                [name.lower()]
            )
        ).fetchone()[0] == 1

    def create_table(self, name):
        self.adb.safe_execute(
            self.ticket,
            lambda db, cursor: cursor.execute(
                """
                CREATE TABLE {} (
                    "id"        INTEGER NOT NULL UNIQUE,
                    "kid"       TEXT NOT NULL COLLATE NOCASE,
                    "key_"      TEXT NOT NULL COLLATE NOCASE,
                    "title"     TEXT NULL,
                    PRIMARY KEY("id" AUTOINCREMENT),
                    UNIQUE("kid", "key_")
                );
                """.format(name.lower())
            )
        )


parser = argparse.ArgumentParser()
parser.add_argument(
    "-i", "--input",
    help="vault",
    required=True)
args = parser.parse_args()

LocalVault(args.input)
```

### `scripts\migrate_credentials.py`

```python

```

### `scripts\ClientIDGen\ClientIDGen.py`

```python
#!/usr/bin/env python3

import argparse
import base64

import yaml

from pywidevine.protos.widevine_pb2 import ClientIdentificationRaw

parser = argparse.ArgumentParser("Widevine Client ID building tool.")
parser.add_argument("-q", "--quiet",
                    help="do not print the generated client id",
                    action="store_true")
parser.add_argument("-c", "--config",
                    help="configuration yaml file",
                    default="config.yml")
parser.add_argument("-o", "--output",
                    default="device_client_id_blob",
                    help="output filename")
args = parser.parse_args()

with open(args.config) as fd:
    config = yaml.safe_load(fd)

with open(config["token"], "rb") as fd:
    token = fd.read()

ci = ClientIdentificationRaw()
ci.Type = ClientIdentificationRaw.DEVICE_CERTIFICATE
ci.Token = token

for name, value in config["client_info"].items():
    nv = ci.ClientInfo.add()
    nv.Name = name
    if name == "device_id":
        value = base64.b64decode(value)
    nv.Value = value

capabilities = ClientIdentificationRaw.ClientCapabilities()
caps = config["capabilities"]
if "client_token" in caps:
    capabilities.ClientToken = caps["client_token"]
if "session_token" in caps:
    capabilities.SessionToken = caps["session_token"]
if "video_resolution_constraints" in caps:
    capabilities.VideoResolutionConstraints = caps["video_resolution_constraints"]
if "max_hdcp_version" in caps:
    max_hdcp_version = caps["max_hdcp_version"]
    if str(max_hdcp_version).isdigit():
        max_hdcp_version = int(max_hdcp_version)
    else:
        max_hdcp_version = ClientIdentificationRaw.ClientCapabilities.HdcpVersion.Value(max_hdcp_version)
    capabilities.MaxHdcpVersion = max_hdcp_version
if "oem_crypto_api_version" in caps:
    capabilities.OemCryptoApiVersion = int(caps["oem_crypto_api_version"])
# I have not seen any of the following in use:
if "anti_rollback_usage_table" in caps:
    capabilities.AntiRollbackUsageTable = caps["anti_rollback_usage_table"]
if "srm_version" in caps:
    capabilities.SrmVersion = int(caps["srm_version"])
if "can_update_srm" in caps:
    capabilities.ClientToken = caps["can_update_srm"]
# is it possible to refactor this?
if "supported_certificate_key_type" in caps:
    supported_certificate_key_type = caps["supported_certificate_key_type"]
    if str(supported_certificate_key_type).isdigit():
        supported_certificate_key_type = int(supported_certificate_key_type)
    else:
        supported_certificate_key_type = ClientIdentificationRaw.ClientCapabilities.CertificateKeyType.Value(
            supported_certificate_key_type
        )
    capabilities.SupportedCertificateKeyType.append(supported_certificate_key_type)
ci._ClientCapabilities.CopyFrom(capabilities)

if not args.quiet:
    print(ci)

with open(args.output, "wb") as fd:
    fd.write(ci.SerializeToString())
```

### `scripts\ClientIDGen\config.example.yml`

```yaml
# NOTE!
# This client id gen script may use outdated ClientIdentification values.
# Just letting you know, do whatever you wish, but yeah

token: 'token.bin'

client_info:
  company_name: 'motorola'
  model_name: 'Nexus 6'
  architecture_name: 'armeabi-v7a'
  device_name: 'shamu'
  product_name: 'shamu'
  build_info: 'google/shamu/shamu:5.1.1/LMY48M/2167285:user/release-keys'
  device_id: 'TU1JX0VGRkYwRkU2NUQ5OA=='
  os_version: '5.1.12'

capabilities:
  session_token: 1
  max_hdcp_version: 'HDCP_V2_2'
  oem_crypto_api_version: 11
```

### `scripts\VMPBlobGen\README.md`

```markdown
# VMPBlobGen

Notes on VMP:

- Android doesn't require (or use!) a VMP blob (the oemcrypto hardware backs it and HDCP controls the path)
- Chrome and WidevineCDM both have signature files. The widevinecdm.dll and chrome.exe sign both the signature files,
  then sign with the private key and inject to the license request in field 7, but you need a server cert to encrypt
  the challenge otherwise.
```

### `scripts\VMPBlobGen\VMPBlobGen.py`

```python
#!/usr/bin/env python3

import os
import sys
from hashlib import sha512

from pywidevine.protos.widevine_pb2 import FileHashes
from pywidevine.vmp import WidevineSignatureReader

"""
Script that generates a VMP blob for chromecdm
"""

WIN32_FILES = [
    "chrome.exe",
    "chrome.dll",
    "chrome_child.dll",
    "widevinecdmadapter.dll",
    "widevinecdm.dll"
]


def sha512file(filename):
    """Compute SHA-512 digest of file."""
    sha = sha512()
    with open(filename, "rb") as fd:
        for b in iter(lambda: fd.read(0x10000), b''):
            sha.update(b)
    return sha.digest()


def build_vmp_field(filenames):
    """
    Create and fill out a FileHashes object.

    `filenames` is an array of pairs of filenames like (file, file_signature)
    such as ("module.dll", "module.dll.sig"). This does not validate the signature
    against the codesign root CA, or even the sha512 hash against the current signature+signer
    """
    file_hashes = FileHashes()

    for basename, file, sig in filenames:
        signature = WidevineSignatureReader.from_file(sig)
        s = file_hashes.signatures.add()
        s.filename = basename
        s.test_signing = False  # we can't check this without parsing signer
        s.SHA512Hash = sha512file(file)
        s.main_exe = signature.mainexe
        s.signature = signature.signature

    file_hashes.signer = signature.signer
    return file_hashes.SerializeToString()


def get_files_with_signatures(path, required_files=None, random_order=False, sig_ext="sig"):
    """
    use on chrome dir (a given version).
    random_order would put any files it found in the dir with sigs,
    it's not the right way to do it and the browser does not do this.
    this function can still fail (generate wrong output) in subtle ways if
    the Chrome dir has copies of the exe/sigs, especially if those copies are modified in some way
    """
    if not required_files:
        required_files = WIN32_FILES

    all_files = []
    sig_files = []
    for dir_path, _, filenames in os.walk(path):
        for filename in filenames:
            full_path = os.path.join(dir_path, filename)
            all_files.append(full_path)
            if filename.endswith(sig_ext):
                sig_files.append(full_path)

    base_names = []
    for path in sig_files:
        orig_path = os.path.splitext(path)[0]
        if orig_path not in all_files:
            print("signature file {} lacks original file {}".format(path, orig_path))
        base_names.append(path.name)

    if not set(base_names).issuperset(set(required_files)):
        # or should just make this warn as the next exception would be more specific
        raise ValueError("Missing a binary/signature pair from {}".format(required_files))

    files_to_hash = []
    if random_order:
        for path in sig_files:
            orig_path = os.path.splitext(path)[0]
            files_to_hash.append((os.path.basename(orig_path), orig_path, path))
    else:
        for basename in required_files:
            found_file = False
            for path in sig_files:
                orig_path = os.path.splitext(path)[0]
                if orig_path.endswith(basename):
                    files_to_hash.append((basename, orig_path, path))
                    found_file = True
                    break
            if not found_file:
                raise Exception("Failed to locate a file sig/pair for {}".format(basename))

    return files_to_hash


def make_vmp_buff(browser_dir, file_msg_out):
    with open(file_msg_out, "wb") as fd:
        fd.write(build_vmp_field(get_files_with_signatures(browser_dir)))


if len(sys.argv) < 3:
    print("Usage: {} BrowserPathWithVersion OutputPBMessage.bin".format(sys.argv[0]))
else:
    make_vmp_buff(sys.argv[1], sys.argv[2])
```

### `scripts\WVD\JsonWVDtoStructWVD.py`

```python
#!/usr/bin/env python3

import argparse
import base64
import json
import os

from pywidevine.device import LocalDevice

"""
Code to convert common folder/file structure to a vinetrimmer WVD.
"""

parser = argparse.ArgumentParser(
    "JsonWVDtoStructWVD",
    description="Simple script to read cdm data from old wvd json and write it into a new WVD struct file."
)
parser.add_argument(
    "-i", "--input",
    help="path to wvd json file",
    required=False)
parser.add_argument(
    "-d", "--dir",
    help="path to MULTIPLE wvd json files",
    required=False)
args = parser.parse_args()

files = []
if args.dir:
    files.extend(os.listdir(args.dir))
elif args.input:
    files.append(args.input)

for file in files:
    if not file.lower().endswith(".wvd") or os.path.splitext(file)[0].endswith(".struct"):
        continue

    if not os.path.isfile(file):
        raise ValueError("Not a file or doesn't exist...")

    print(f"Generating wvd struct file for {file}...")

    with open(file, encoding="utf-8") as fd:
        wvd_json = json.load(fd)

    device = LocalDevice(
        type=LocalDevice.Types[wvd_json["device_type"].upper()],
        security_level=wvd_json["security_level"],
        flags={
            "send_key_control_nonce": wvd_json["send_key_control_nonce"]
        },
        private_key=base64.b64decode(wvd_json["device_private_key"]),
        client_id=base64.b64decode(wvd_json["device_client_id_blob"]),
        vmp=base64.b64decode(wvd_json["device_vmp_blob"]) if wvd_json.get("device_vmp_blob") else None
    )

    out = os.path.join(os.path.dirname(file), "structs", os.path.basename(file))
    os.makedirs(os.path.dirname(out), exist_ok=True)

    device.dump(out)

    print(device)
    print(f"Done: {file}")

print("Done")
```

### `scripts\WVD\MakeWVD.py`

```python
#!/usr/bin/env python3

import argparse
import json
import os
import re
import sys

from pywidevine.device import LocalDevice

"""
Code to convert common folder/file structure to a vinetrimmer WVD.
"""

parser = argparse.ArgumentParser()
parser.add_argument("dirs", metavar="DIR", nargs="+", help="Directory containing device files")
args = parser.parse_args()

configs = []
for d in args.dirs:
    for root, dirs, files in os.walk(d):
        for f in files:
            if f == "wv.json":
                configs.append(os.path.join(root, f))

if not configs:
    print("No wv.json file found in any of the specified directories.")
    sys.exit(1)

for f in configs:
    d = os.path.dirname(f)

    print(f"Generating WVD struct file for {os.path.abspath(d)}...")

    with open(f, encoding="utf-8") as fd:
        config = json.load(fd)

    device = LocalDevice.from_dir(d)

    # we cannot output to /data/CDM_Devices etc. as the CWD might not align up
    # also best to keep the security level and system id definition on the filename for easy referencing
    name = re.sub(r"_lvl\d$", "", config["name"])
    out_path = f"{name}_l{device.security_level}_{device.system_id}.wvd"

    device.dump(out_path)

    print(device)

    print(f"Done, saved to: {os.path.abspath(out_path)}")
    print()
```

### `wpgskd\__init__.py`

```python
__version__ = "0.2.0"
```

### `wpgskd\constants.py`

```python
from enum import Enum

class EncryptionScheme(Enum):
    NONE = "none"
    WIDEVINE = "widevine"
    PLAYREADY = "playready"
    CLEARKEY = "clearkey"
    AES_128 = "aes-128"
    AES_128_ECB = "aes-128-ecb"
    SAMPLE_AES = "SAMPLE-AES"

LANGUAGE_MUX_MAP = {
    "none": "und",
    "nb": "nor",
}

TERRITORY_MAP = {
    "001": "",
    "150": "European",
    "419": "Latin American",
    "AU": "Australian",
    "BE": "Flemish",
    "BR": "Brazilian",
    "CA": "Canadian",
    "CZ": "",
    "CN": "Chinese Mainland",
    "DK": "",
    "EG": "Egyptian",
    "ES": "European",
    "FR": "European",
    "GB": "British",
    "GR": "",
    "HK": "Hong Kong",
    "IL": "",
    "IN": "",
    "JP": "Japan",
    "KR": "",
    "MY": "",
    "NO": "",
    "PH": "",
    "PS": "Palestinian",
    "PT": "European",
    "SE": "",
    "SY": "Syrian",
    "TW": "Taiwan",
    "US": "American",
}

LANGUAGE_MAX_DISTANCE = 5

CODEC_MAP = {
    "avc1": "H.264", "avc3": "H.264", "hev1": "H.265", "hvc1": "H.265", "dvh1": "H.265", "dvhe": "H.265", "av01": "AV1",
    "aac": "AAC", "mp4a": "AAC", "stereo": "AAC", "HE": "HE-AAC", "ac3": "AC3", "ac-3": "AC3", "dd": "DD",
    "eac": "E-AC3", "eac3": "E-AC3", "eac-3": "E-AC3", "ec-3": "DD+", "ddp": "DD+", "dd+": "DD+", "atmos": "DD+ Atmos", "ec3": "DD+",
    "srt": "SRT", "vtt": "VTT", "wvtt": "WVTT", "dfxp": "TTML", "stpp": "TTML", "ttml": "TTML", "tt": "TTML", "ass": "ASS", "ssa": "SSA",
}
```

### `wpgskd\wpgskd.py`

```python
import logging
import os
import sys
import warnings
from datetime import datetime

warnings.filterwarnings("ignore", category=UserWarning, module='pproxy')
warnings.filterwarnings("ignore", message=".*pkg_resources is deprecated.*")

import click
import coloredlogs

from wpgskd.config import directories, filenames
from wpgskd.commands.dl import dl

@click.group(context_settings=dict(
    allow_extra_args=True,
    ignore_unknown_options=True,
    max_content_width=116,
))
@click.option("--debug", is_flag=True, default=False,
              help="Enable DEBUG level logs on the console. This is always enabled for log files.")
def main(debug):
    """
    WPGSKD - Widevine PlayReady General Stream Key Decryptor
    """
    LOG_FORMAT = "{asctime} [{levelname[0]}] {name} : {message}"
    LOG_DATE_FORMAT = "%Y-%m-%d %H:%M:%S"
    LOG_STYLE = "{"

    def log_exit(self, msg, *args, **kwargs):
        self.critical(msg, *args, **kwargs)
        sys.exit(1)

    logging.Logger.exit = log_exit

    os.makedirs(directories.logs, exist_ok=True)
    logging.basicConfig(
        level=logging.DEBUG,
        format=LOG_FORMAT,
        datefmt=LOG_DATE_FORMAT,
        style=LOG_STYLE,
        handlers=[logging.FileHandler(
            os.path.join(directories.logs, filenames.log.format(time=datetime.now().strftime("%Y%m%d-%H%M%S"))),
            encoding='utf-8'
        )]
    )

    coloredlogs.install(
        level=logging.DEBUG if debug else logging.INFO,
        fmt=LOG_FORMAT,
        datefmt=LOG_DATE_FORMAT,
        style=LOG_STYLE,
        handlers=[logging.StreamHandler()],
    )

    log = logging.getLogger("wpgskd")

    log.info("WPGSKD - Widevine, PlayReady, AES-128 & ClearKey Downloader")
    log.info(f"[Root Config]     : {filenames.user_root_config}")
    log.info(f"[Cookies]         : {directories.cookies}")
    log.info(f"[CDM Devices]     : {directories.devices}")
    log.info(f"[Cache]           : {directories.cache}")
    log.info(f"[Logs]            : {directories.logs}")
    log.info(f"[Temp Files]      : {directories.temp}")
    log.info(f"[Downloads]       : {directories.downloads}")
    
    bin_path = os.path.abspath('./binaries')
    if os.path.exists(bin_path):
        os.environ['PATH'] += os.pathsep + bin_path


@main.group(name="tools")
def tools():
    pass

@tools.command(name="merge-vault")
@click.option("-i", "--input", "input_db", required=True, type=click.Path(exists=True))
@click.option("-o", "--output", "output_db", required=True, type=click.Path())
def merge_vault(input_db, output_db):
    from wpgskd.core.vaults import Vaults, LocalVault
    
    log = logging.getLogger("tools")
    log.info(f"Merging keys from {input_db} to {output_db}")
    
    src_vault = LocalVault(name="Source", path=input_db)
    dst_vault = LocalVault(name="Target", path=output_db)
    
    conn = src_vault.con
    cursor = conn.cursor()
    cursor.execute("SELECT name FROM sqlite_master WHERE type='table' AND name NOT LIKE 'sqlite_%'")
    tables = cursor.fetchall()
    
    total_added, total_skipped = 0, 0
    for table_row in tables:
        table = table_row[0]
        cursor.execute(f"SELECT kid, key_, title FROM `{table}`")
        rows = cursor.fetchall()
        
        added, skipped = 0, 0
        for kid, key, title in rows:
            res = dst_vault.insert_key(table, kid, key, title, commit=False)
            if res.name == "SUCCESS": added += 1
            else: skipped += 1
            
        dst_vault.commit()
        total_added += added
        total_skipped += skipped
        log.info(f"  Table [{table}]: Added {added}, Skipped {skipped}")

    log.info(f"Merge complete! Total Added: {total_added}, Total Skipped: {total_skipped}")


@tools.command(name="add-keys")
@click.option("-t", "--table", "service", required=True, help="Service name (e.g. netflix, amazon)")
@click.option("-i", "--input", "input_file", type=click.Path(exists=True))
@click.option("-o", "--output", "output_db", required=True, type=click.Path())
def add_keys(service, input_file, output_db):
    import re
    from wpgskd.core.vaults import LocalVault
    
    log = logging.getLogger("tools")
    vault = LocalVault(name="Target", path=output_db)
    
    added, skipped = 0, 0
    pattern = re.compile(r"^(?P<kid>[0-9a-fA-F]{32}):(?P<key>[0-9a-fA-F]{32})(:(?P<title>[\w .:-]*))?$")
    
    with open(input_file, "r", encoding="utf-8") as f:
        for line in f:
            m = pattern.match(line.strip())
            if not m: continue
            kid = m.group("kid").lower()
            key = m.group("key").lower()
            title = m.group("title")
            
            res = vault.insert_key(service, kid, key, title, commit=False)
            if res.name == "SUCCESS": added += 1
            else: skipped += 1
            
    vault.commit()
    log.info(f"Batch add complete. Added: {added}, Skipped: {skipped}")


main.add_command(dl)

if __name__ == "__main__":
    main()
```

### `wpgskd\wpgskd.yml`

```yaml
decrypter: 'mp4decrypt'
tag: ''
tag_sd: ''

arguments: {}

aria2c:
  file_allocation: 'prealloc'
  

cdm:
  default: 'default'


credentials:
  HBOMax: 'email:password'
  ADN: 'email:password'
  Crunchyroll: 'email:password'
  Netflix: 'email:password'
  Crave: 'email:password'
  Videoland: 'email:password'
  DisneyPlus: 'email:password'
  ParamountPlus: 'email:password'
  All4: 'email:password'
  RakutenTV: 'email:password'
  BritBox: 'email:password'
  TSUBURAYA: 'email:password'
  DMMTV: 'email:password'

directories:
  temp: ''
  downloads: ''

headers:
  User-Agent: 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/147.0.0.0 Safari/537.36'

key_vaults:
  - type: 'local'
    name: 'Local'
    path: '{data_dir}/key_store.db'

  - type: 'httpapi'
    name: vault
    host: https://drmwpvault.xin
    password:

output_template:
  movies: '{title}.{year}.{quality}.{source}.WEB-DL.{audio}.{video}-{tag}'
  series: '{title}.{season_episode}.{episode_name}.{quality}.{source}.WEB-DL.{audio}.{video}-{tag}'
  use_last_audio: false

profiles:
  default: 'default'
  TVer: false
  AbemaTV: false
  
default_proxy_service: null  # Options: 'surfshark', 'nordvpn'

proxies: {}

nordvpn:
    #username: ''
    #password: ''

surfshark:
    #username: ''
    #password: ''

```

### `wpgskd\commands\click_utils.py`

```python
import re
import logging
import click
from wpgskd import servicookies as services
from wpgskd.core.collections import as_list

log = logging.getLogger("click")

class ContextData:
    def __init__(self, config, vaults, cdm, profile=None, cookies=None, credentials=None):
        self.config = config
        self.vaults = vaults
        self.cdm = cdm
        self.profile = profile
        self.cookies = cookies
        self.credentials = credentials

class AliasedGroup(click.Group):
    def get_command(self, ctx, cmd_name):
        rv = click.Group.get_command(self, ctx, cmd_name)
        if rv is not None:
            return rv

        for key, aliases in services.SERVICE_MAP.items():
            if cmd_name.lower() in map(str.lower, aliases):
                if hasattr(services, key):
                    service_cls = getattr(services, key)
                    if hasattr(service_cls, 'cli'):
                        return service_cls.cli
                return None

        service_key = services.get_service_key(cmd_name)
        if not service_key:
            for name in services.SERVICE_MAP:
                if hasattr(services, name):
                    service_cls = getattr(services, name)
                    title_re = as_list(getattr(service_cls, "TITLE_RE", []))
                    for regex in title_re:
                        m = re.search(regex, cmd_name)
                        if m and m.group().startswith(("http://", "https://", "urn:")):
                            service_key = name
                            ctx.params["service_name"] = name
                            if "id" in m.groupdict():
                                ctx.params["title"] = m.group("id")
                            else:
                                ctx.params["title"] = cmd_name
                            break
                if service_key:
                    break

        if service_key and hasattr(services, service_key):
            service_cls = getattr(services, service_key)
            if hasattr(service_cls, 'cli'):
                return service_cls.cli

    def list_commands(self, ctx):
        return sorted(self.commands, key=str.casefold)

def _choice(ctx, param, value, value_map):
    if value is None: return None
    if value.lower() in value_map:
        return value_map[value.lower()]
    else:
        valid_values = {x: None for x in value_map.values()}
        valid_values = ", ".join(repr(x) for x in valid_values)
        ctx.fail(f"Invalid value for {param.name!r}: {value!r} is not one of {valid_values}.")

def acodec_param(ctx, param, value):
    return _choice(ctx, param, value, {
        "aac": "AAC", "ac3": "AC3", "ac-3": "AC3", "dd": "AC3",
        "ec3": "EC3", "ec-3": "EC3", "eac3": "EC3", "e-ac3": "EC3", "e-ac-3": "EC3", "dd+": "EC3", "ddp": "EC3",
        "vorb": "VORB", "vorbis": "VORB", "opus": "OPUS", "flac": "FLAC",
    })

def channels_param(ctx, param, value):
    return _choice(ctx, param, value, {
        "2": "2.0", "2.0": "2.0", "5.1": "5.1", "6": "5.1",
        "7.1": "7.1", "atmos": "16/JOC", "16/joc": "16/JOC",
    })

def language_param(ctx, param, value):
    if isinstance(value, list): return value
    if not value: return []
    return re.split(r"\s*[,;]\s*", value)

def quality_param(ctx, param, value):
    if not value: return None
    if value.lower() == "sd": return "SD"
    if value.lower() == "hd720": return "HD720"
    if value.lower() == "4k": return 2160
    try:
        return int(value.lower().rstrip("p"))
    except TypeError:
        ctx.fail(f"expected string for int() conversion, got {value!r}", param, ctx)
    except ValueError:
        ctx.fail(f"{value!r} is not a valid integer", param, ctx)

def range_param(ctx, param, value):
    return _choice(ctx, param, value, {
        "sdr": "SDR", "hdr": "HDR10", "hdr10": "HDR10",
        "hdr10+": "HDR10+", "hdr10plus": "HDR10+",
        "hlg": "HLG", "dv": "DV", "dovi": "DV",
        "dv+hdr": "DV+HDR", "dvhdr": "DV+HDR"
    })

def vcodec_param(ctx, param, value):
    return _choice(ctx, param, value, {
        "h264": "H264", "avc": "H264", "h265": "H265", "hevc": "H265",
        "vp9": "VP9", "av1": "AV1",
    })

def wanted_param(ctx, param, value):
    MIN_EPISODE = 0
    MAX_EPISODE = 9999

    def parse_tokens(*tokens):
        if len(tokens) == 0: return []
        computed, exclusions = [], []
        for token in tokens:
            exclude = token.startswith("-")
            if exclude: token = token[1:]
            parsed = [re.match(r"^S(?P<season>\d+)(E(?P<episode>\d+))?$", x, re.IGNORECASE) for x in re.split(r"[:-]", token)]
            if len(parsed) > 2: ctx.fail(f"Invalid token: {token}")
            if len(parsed) == 1: parsed.append(parsed[0])
            if any(x is None for x in parsed): ctx.fail(f"Invalid token syntax: {token}")
            
            from_season, from_episode = [int(v) if v is not None else MIN_EPISODE for k, v in parsed[0].groupdict().items() if parsed[0]]
            to_season, to_episode = [int(v) if v is not None else MAX_EPISODE for k, v in parsed[1].groupdict().items() if parsed[1]]
            
            if from_season > to_season: ctx.fail(f"Invalid range: {token}")
            if from_season == to_season and from_episode > to_episode: ctx.fail(f"Invalid range: {token}")
            
            for s in range(from_season, to_season + 1):
                for e in range(from_episode if s == from_season else 0, (MAX_EPISODE if s < to_season else to_episode) + 1):
                    (computed if not exclude else exclusions).append(f"{s}x{e}")
                    
        for exclusion in exclusions:
            if exclusion in computed: computed.remove(exclusion)
        return list(set(computed))

    if value:
        return parse_tokens(*re.split(r"\s*[,;]\s*", value))
```

### `wpgskd\commands\dl.py`

```python
import logging
import math
import os
import random
import time
from pathlib import Path

import click
import requests

from wpgskd import servicookies as services
from wpgskd.config import config, directories, filenames
from wpgskd.core.cdm.loader import CdmProvider
from wpgskd.core.console import ConsoleUI
from wpgskd.core.decryptor import Decryptor
from wpgskd.core.downloader import Downloader
from wpgskd.core.events import EventManager, Events
from wpgskd.core.muxer import Muxer
from wpgskd.core.resolver import KeyResolver
from wpgskd.core.tracks.title import Title, Titles
from wpgskd.core.tracks.audio import AudioTrack
from wpgskd.core.tracks.tracks import TextTrack
from wpgskd.core.vault import LocalVault
from wpgskd.core.vaults import Vaults
from wpgskd.commands.click_utils import (AliasedGroup, ContextData, acodec_param,
                                channels_param, language_param, quality_param,
                                range_param, vcodec_param, wanted_param)

log = logging.getLogger("dl")

@click.group(name="dl", short_help="Download from a service.", cls=AliasedGroup, context_settings=dict(
    help_option_names=["-?", "-h", "--help"],
    max_content_width=116,
    default_map=config.arguments
))
@click.option("--debug", is_flag=True, hidden=True)
@click.option("-p", "--profile", type=str, default=None,
              help="Profile to use when multiple profiles are defined for a service.")
@click.option("-q", "--quality", callback=quality_param, default=None,
              help="Download Resolution, defaults to best available.")
@click.option("-v", "--vcodec", callback=vcodec_param, default="H264",
              help="Video Codec, defaults to H264.")
@click.option("-a", "--acodec", callback=acodec_param, default=None,
              help="Audio Codec")
@click.option("-vb", "--vbitrate", "vbitrate", type=int, default=None,
              help="Video Bitrate, defaults to Max.")
@click.option("-ab", "--abitrate", "abitrate", type=int, default=None,
              help="Audio Bitrate, defaults to Max.")
@click.option("-aa", "--atmos", is_flag=True, default=False,
              help="Prefer Atmos Audio")
@click.option("-ch", "--channels", callback=channels_param, default=None,
              help="Audio Channels")
@click.option("-r", "--range", "range_", callback=range_param, default="SDR",
              help="Video Color Range, defaults to SDR.")
@click.option("-w", "--wanted", callback=wanted_param, default=None,
              help="Wanted episodes, e.g. `S01-S05,S07`, `S01E01-S02E03`, defaults to all.")
@click.option("-al", "--alang", callback=language_param, default="orig",
              help="Language wanted for audio.")
@click.option("-sl", "--slang", callback=language_param, default="all",
              help="Language wanted for subtitles.")
@click.option("--delay", type=int, default=None,
              help="Delay between title processing")
@click.option("--proxy", type=str, default=None,
              help="Proxy URI to use. If a 2-letter country is provided, it will try get a proxy from the config.")
@click.option("-A", "--audio-only", is_flag=True, default=False, help="Only download audio tracks.")
@click.option("-S", "--subs-only", is_flag=True, default=False, help="Only download subtitle tracks.")
@click.option("-C", "--chapters-only", is_flag=True, default=False, help="Only download chapters.")
@click.option("-ns", "--no-subs", is_flag=True, default=False, help="Do not download subtitle tracks.")
@click.option("-na", "--no-audio", is_flag=True, default=False, help="Do not download audio tracks.")
@click.option("-nv", "--no-video", is_flag=True, default=False, help="Do not download video tracks.")
@click.option("-nc", "--no-chapters", is_flag=True, default=False, help="Do not download chapters tracks.")
@click.option("-ad", "--audio-description", is_flag=True, default=False, help="Download audio description tracks.")
@click.option("--list", "list_", is_flag=True, default=False, help="List available tracks without downloading.")
@click.option("--selected", is_flag=True, default=False, help="List selected tracks without downloading.")
@click.option("--cdm", type=str, default=None, help="Override the CDM that will be used for decryption.")
@click.option("--export", "export_arg", is_flag=False, flag_value="", default=None,
              help="Export track info and decryption keys to a JSON file. Can optionally specify file name.")
@click.option("--keys", is_flag=True, default=False, help="Skip downloading, retrieve keys and print them.")
@click.option("--cache", is_flag=True, default=False, help="Disable CDM use, only retrieve keys from Key Vaults.")
@click.option("--no-cache", is_flag=True, default=False, help="Disable Key Vaults use, only retrieve keys from CDM.")
@click.option("--no-proxy", is_flag=True, default=False, help="Force disable all proxy use.")
@click.option("--force-proxy", is_flag=True, default=False, help="Force using proxy even if current region matches.")
@click.option("-nm", "--no-mux", is_flag=True, default=False, help="Do not mux the downloaded and decrypted tracks.")
@click.option("--mux", is_flag=True, default=False, help="Force muxing when using --audio-only/--subs-only/--chapters-only.")
@click.option("--worst", is_flag=True, default=False, help="Choose the worst available video tracks rather than the best")
@click.option("--sync-vat", is_flag=True, default=False, help="Compress audio duration to match video duration before muxing.")
@click.option("-nys", "--no-sync-subs", is_flag=True, default=False, help="Do not merge/sync subtitle tracks during muxing.")
@click.pass_context
def dl(ctx, profile, cdm, *_, **__):
    """Download from a specified service."""
    if ctx.params.get("debug"):
        import coloredlogs
        LOG_FORMAT = "{asctime} [{levelname[0]}] {name} : {message}"
        LOG_DATE_FORMAT = "%Y-%m-%d %H:%M:%S"
        LOG_STYLE = "{"
        coloredlogs.install(
            level=logging.DEBUG,
            fmt=LOG_FORMAT,
            datefmt=LOG_DATE_FORMAT,
            style=LOG_STYLE,
            handlers=[logging.StreamHandler()]
        )
        
    service_name = ctx.params.get("service_name") or services.get_service_key(ctx.invoked_subcommand)
    if not service_name:
        log.error(" - Unable to find service")
        return

    profile = profile or config.profiles.get(service_name) or config.profiles.get("default") or "default"
    
    service_config = services.get_service_config(service_name)

    vaults_list = []
    for vault_cfg in config.key_vaults:
        try:
            vaults_list.append(Vaults.load_vault(vault_cfg))
        except Exception as e:
            log.error(f" - Failed to load vault {vault_cfg.get('name')!r}: {e}")
    
    vaults_obj = Vaults(vaults_list, service=service_name)
    local_count = sum(1 for v in vaults_obj.vaults if isinstance(v, LocalVault))
    remote_count = sum(1 for v in vaults_obj.vaults if not isinstance(v, LocalVault))
    log.info(f" + {local_count} Local, {remote_count} Remote Vault(s) loaded")

    cdm_cfg_dict = {k.lower(): v for k, v in config.cdm.items()}
    cdm_name = cdm or cdm_cfg_dict.get(service_name.lower()) or cdm_cfg_dict.get("default")

    try:
        cdm_prov = CdmProvider(
            cdm_name=cdm_name,
            device_dir=directories.devices,
            cdm_api_config=config.cdm_api
        )
        cdm_prov.log_info()
    except Exception as e:
        log.error(f" - CDM Init Error: {e}")
        raise click.Abort() 
        return

    cookies = credentials_obj = None
    needs_auth = service_config.get("needs_auth", True)
    if profile:
        cookies = services.get_cookie_jar(service_name, profile)
        credentials_obj = services.get_credentials(service_name, profile)
        if not cookies and not credentials_obj and needs_auth:
            log.error(f" - Profile {profile!r} has no cookies or credentials")
            return

    ctx.obj = ContextData(
        config=service_config,
        vaults=vaults_obj,
        cdm=cdm_prov,
        profile=profile,
        cookies=cookies,
        credentials=credentials_obj
    )


@dl.result_callback()
def result(service, quality, vcodec, acodec, range_, wanted, alang, slang,
           audio_only, subs_only, chapters_only, audio_description, list_, keys,
           cache, no_cache, no_subs, no_audio, no_video, no_chapters, atmos,
           vbitrate: int, abitrate: int, channels, no_mux, worst, mux, delay,
           selected, sync_vat, no_sync_subs, export_arg, *_, **__):

    log = service.log
    service_name = service.__class__.__name__

    log.info("Retrieving Titles")
    try:
        titles = Titles(service.get_titles())
    except requests.HTTPError as e:
        log.error(f" - HTTP Error {e.response.status_code}: {e.response.reason}")
        return
        
    if not titles:
        log.error(" - No titles returned!")
        return
        
    titles.order()
    ConsoleUI.print_titles(titles)

    cdm_prov: CdmProvider = service.cdm
    resolver = KeyResolver(
        vaults=service.vaults,
        cdm_provider=cdm_prov,
        use_cache=not no_cache,
        use_cdm=not cache
    )
    downloader = Downloader(session=service.session)

    first = True
    for title in titles.with_wanted(wanted):
        if not first and delay:
            jitter = random.randint(math.floor(-delay / 5), math.floor(delay / 5))
            d = delay + jitter
            log.info(f"Delaying for {d}s before getting next title...")
            time.sleep(d)
        first = False

        _log_title(log, title)

        try:
            title.tracks.add(service.get_tracks(title), warn_only=True)
            chapters = service.get_chapters(title)
            if chapters:
                title.tracks.add(chapters)
        except requests.HTTPError as e:
            log.error(f" - HTTP Error getting tracks: {e.response.status_code}")
            continue

        title.tracks.sort_videos()
        title.tracks.sort_audios(by_language=alang)
        title.tracks.sort_subtitles(by_language=slang)
        title.tracks.sort_chapters()
        
        for track in title.tracks:
            track.is_original_lang = track.language == title.original_lang

        if not list(title.tracks):
            log.error(" - No tracks returned!")
            continue

        if not selected:
            log.info("> All Tracks:")
            ConsoleUI.print_tracks(title.tracks, title)

        try:
            if range_ == "DV+HDR":
                title.tracks.select_videos_multi(["HDR10", "DV"], by_quality=quality, by_vbitrate=vbitrate)
            else:
                title.tracks.select_videos(
                    by_quality=quality, by_vbitrate=vbitrate, by_range=range_,
                    one_only=True, by_worst=worst, by_codec=vcodec
                )
            title.tracks.select_audios(
                by_language=alang, by_bitrate=abitrate, with_atmos=atmos,
                with_descriptive=audio_description, by_channels=channels, by_codec=acodec
            )
            title.tracks.select_subtitles(by_language=slang, with_forced=True)
        except ValueError as e:
            log.error(f" - {e}")
            continue

        _apply_filters(title, no_video, no_audio, no_subs, no_chapters, audio_only, subs_only, chapters_only, mux)

        log.info("> Selected Tracks:")
        ConsoleUI.print_tracks(title.tracks, title)

        if list_:
            continue

        all_content_keys = {}
        skip_title = False
        
        for track in title.tracks:
            if track.encrypted and str(track.descriptor).split(".")[-1] == "M3U":
                if not track.pssh and not track.pr_pssh:
                    track.get_pssh(service.session)
                    
            enc_scheme = track.encryption_scheme.name if hasattr(track.encryption_scheme, 'name') else track.encryption_scheme
            if not track.encrypted or enc_scheme in ["AES_128", "CLEARKEY"]:
                continue

            log.info(f"Licensing: {str(track).replace('├─ ', '').replace('└─ ', '')}")
            
            if not track.pssh and not track.pr_pssh:
                track.get_pssh(service.session)
                
            if not track.kid:
                track.get_kid(service.session)

            cdm_type = cdm_prov.cdm_instance.cdm_type if cdm_prov else "widevine"

            if cdm_type == "playready":
                if getattr(track, 'pr_pssh', None):
                    pssh_str = track.pr_pssh
                    if isinstance(pssh_str, bytes):
                        pssh_str = pssh_str.decode('utf-8', 'ignore')
                    log.info(f" + PR_PSSH: {pssh_str}")
            else:  # widevine
                if getattr(track, 'pssh', None):
                    pssh_obj = track.pssh
                    try:
                        if hasattr(pssh_obj, 'dumps') and callable(pssh_obj.dumps):
                            dumped = pssh_obj.dumps()
                            if isinstance(dumped, bytes):
                                import base64
                                log.info(f" + WV_PSSH: {base64.b64encode(dumped).decode('utf-8')}")
                            else:
                                log.info(f" + WV_PSSH: {dumped}")
                        else:
                            log.info(f" + WV_PSSH: {pssh_obj}")
                    except Exception:
                        log.info(f" + WV_PSSH: {pssh_obj}")
            
            if getattr(track, 'kid', None):
                log.info(f" + KID: {track.kid}")

            try:
                pk, akeys = resolver.resolve(track, title, service, service_name, service.session)
                if cache and not pk:
                    skip_title = True
                    break
                
                if pk:
                    track.key = pk
                    all_content_keys.update(akeys)
                    log.info(f" + KEY: {pk[:32]}... (Resolved)")
                else:
                    log.error(" - No content key returned")
                    return
            except Exception as e:
                log.error(f" - Key Resolution Failed: {e}")
                return

        if skip_title:
            for track in title.tracks:
                track.delete()
            continue
            
        if export_arg is not None:
            _export_keys(
                directories.exports, service_name, title, all_content_keys, 
                export_arg, 
                cli_title_id=getattr(service, "title", ""),
                quality=quality,
                vcodec=vcodec,
                range_=range_
            )
            
        if keys:
            continue

        EventManager.publish(Events.BEFORE_DOWNLOAD, title)

        for track in title.tracks:
            log.info(f"\nDownloading: {track}")
            
            proxy = None
            if track.needs_proxy:
                proxy = next(iter(service.session.proxies.values()), None)

            try:
                downloader.download(track, directories.temp, proxy=proxy, title_ref=title, all_keys=all_content_keys)
                log.info(" + Downloaded")
                EventManager.publish(Events.AFTER_DOWNLOAD, track)
            except Exception as e:
                log.error(f" - Download failed: {e}")
                continue

            should_decrypt = track.encrypted and enc_scheme not in ["AES_128", "AES_128_ECB", "CLEARKEY"]
            if should_decrypt:
                log.info("Decrypting...")
                dec_keys = {track.kid.lower().replace("-", ""): track.key.lower()}
                dec_keys.update({k.lower(): v.lower() for k, v in all_content_keys.items()})
                
                try:
                    dec_path = Decryptor.decrypt(track, dec_keys, config.decrypter, directories.temp)
                    if dec_path and track.swap(dec_path):
                        log.info(" + Decrypted")
                        EventManager.publish(Events.AFTER_DECRYPT, track)
                        
                        if track.needs_repack or config.decrypter == "mp4decrypt":
                            log.info("Repackaging stream with FFmpeg")
                            Decryptor.repackage(track.locate())
                            log.info(" + Repackaged")
                    else:
                        log.warning(" - Decryption swap failed")
                except Exception as e:
                    log.error(f" - Decryption failed: {e}")

            if isinstance(track, TextTrack) and track.locate():
                log.info("Converting subtitle to SRT...")
                try:
                    track.convert_to_srt(strip_sdh=False)
                    if track.codec == "srt":
                        log.info(" + Converted to SRT")
                except Exception as e:
                    log.warning(f" - Subtitle conversion failed: {e}")

        if range_ == "DV+HDR":
            try:
                if not any(v.dv and v.hdr10 for v in title.tracks.videos):
                    pass
            except Exception as e:
                log.warning(f" - Skipped DV+HDR: {e}")

        if not list(title.tracks) and not title.tracks.chapters:
            continue

        EventManager.publish(Events.BEFORE_MUX, title)
        
        if no_mux:
            _output_unmuxed(title, log)
        else:
            _output_muxed(title, log, audio_only, subs_only, service_name, sync_vat, no_sync_subs)
            EventManager.publish(Events.AFTER_MUX, title)

    log.info("Processed all titles!")

def _log_title(logger, title: Title):
    if title.type == Title.Types.TV:
        ep = f" - {title.episode_name}" if title.episode_name else ""
        logger.info(f"Getting tracks for {title.name} S{title.season or 0:02}E{title.episode or 0:02}{ep} [{title.id}]")
    else:
        yr = f" ({title.year})" if title.year else ""
        logger.info(f"Getting tracks for {title.name}{yr} [{title.id}]")

def _apply_filters(title, nv, na, ns, nc, ao, so, co, mux):
    if nv: title.tracks.videos.clear()
    if na: title.tracks.audios.clear()
    if ns: title.tracks.subtitles.clear()
    if nc: title.tracks.chapters.clear()
    if ao or so or co:
        title.tracks.videos.clear()
        if ao:
            if not so: title.tracks.subtitles.clear()
            if not co: title.tracks.chapters.clear()
        elif so:
            if not ao: title.tracks.audios.clear()
            if not co: title.tracks.chapters.clear()
        elif co:
            if not ao: title.tracks.audios.clear()
            if not so: title.tracks.subtitles.clear()

def _output_unmuxed(title: Title, logger):
    out_dir = Path(directories.downloads)
    if title.type == Title.Types.TV:
        out_dir = out_dir / title.parse_filename(folder=True)
    out_dir.mkdir(parents=True, exist_ok=True)

    if title.tracks.chapters:
        loc = out_dir / f"{title.parse_filename()}_chapters.txt"
        title.tracks.export_chapters(str(loc))

    for track in title.tracks:
        if not track.locate(): continue
        
        fn = title.parse_filename()
        
        if isinstance(track, TextTrack):
            if track.language:
                fn += f".{track.language}"
            if track.forced:
                fn += ".forced"
            elif track.sdh:
                fn += ".sdh"
                
            ext = "srt" if track.codec == "srt" else Path(track.locate()).suffix[1:].lower()
            if ext not in ["srt", "vtt", "ttml", "ass"]:
                ext = "srt"
                
        elif isinstance(track, AudioTrack):
            if track.language:
                fn += f".{track.language}"
            ext = Path(track.locate()).suffix[1:].lower()
            if ext == "mp4": ext = "m4a"
        else:
            ext = Path(track.locate()).suffix[1:].lower()
            
        target_path = str(out_dir / f"{fn}.{ext}")
        track.move(target_path)

def _output_muxed(title: Title, logger, audio_only, subs_only, service_name, sync_vat, no_sync_subs):
    try:
        muxed_location, returncode = Muxer.mux(title, title.tracks, no_sync_subs=no_sync_subs)
        
        if returncode >= 2:
            logger.error(" - Failed to mux tracks into MKV file")
            return

        logger.info(" + Muxed")
        
        out_dir = Path(directories.downloads)
        if title.type == Title.Types.TV:
            out_dir = out_dir / title.parse_filename(folder=True)
        out_dir.mkdir(parents=True, exist_ok=True)

        base_fn = title.parse_filename()
        ext = "mka" if audio_only else "mks" if subs_only else "mkv"
        target_path = out_dir / f"{base_fn}.{ext}"
        
        import shutil
        shutil.move(muxed_location, str(target_path))
        logger.info(f" + Saved to: {target_path}")

        if sync_vat:
            logger.info("Applying Audio-Video Sync (SyncVAT)...")
            Muxer.apply_sync(str(target_path))

        for track in title.tracks:
            try: track.delete()
            except: pass
        if title.tracks.chapters:
            try: os.unlink(filenames.chapters.format(filename=base_fn))
            except: pass
            
    except Exception as e:
        logger.error(f" - Muxing failed: {e}")
        
def _export_keys(export_dir, service_name, title, all_keys, export_name="", cli_title_id="", quality=None, vcodec=None, range_=None):
    import json
    from pathlib import Path
    from wpgskd.core.tracks.tracks import TextTrack, Track
    
    export_dir = Path(export_dir)
    export_dir.mkdir(parents=True, exist_ok=True)

    if export_name:
        if not export_name.endswith(".json"):
            export_name += ".json"
        export_path = export_dir / export_name
    else:
        parts = [service_name]
        if cli_title_id:
            parts.append(cli_title_id)
        if isinstance(quality, int):
            parts.append(f"{quality}P")
        elif quality:
            parts.append(str(quality).upper())
        if vcodec:
            parts.append(vcodec.upper())
        if range_:
            parts.append(range_.upper())
            
        export_file = "_".join(parts) + ".json"
        export_path = export_dir / export_file
        
    doc = {}
    if export_path.is_file():
        try: 
            doc = json.loads(export_path.read_text(encoding="utf-8"))
        except: pass
            
    titles_dict = doc.setdefault("titles", {})
    tinfo = titles_dict.setdefault(str(title.id), {})
    
    display_name = title.name
    if title.type == Title.Types.TV:
        s_str = f"S{int(title.season):02}" if isinstance(title.season, int) else f"S{title.season}"
        e_str = f"E{int(title.episode):02}" if isinstance(title.episode, int) else f"E{title.episode}"
        display_name = f"{title.name} {s_str}{e_str}"
        if title.episode_name:
            display_name += f" - {title.episode_name}"
            
    tinfo["title_id"] = title.id
    tinfo["title_name"] = display_name
    tinfo["type"] = "TV" if title.type == Title.Types.TV else "MOVIE"
    tinfo["year"] = title.year
    if title.type == Title.Types.TV:
        tinfo["season"] = title.season
        tinfo["number"] = title.episode
        
    tinfo["cbr_manifest_url"] = getattr(title, 'cbr_manifest_url', None)
    tinfo["cvbr_manifest_url"] = getattr(title, 'cvbr_manifest_url', None)
    
    manifest_url = getattr(title, 'manifest_url', None)
    if not manifest_url and title.tracks.videos:
        manifest_url = getattr(title.tracks.videos[0], 'manifest_url', None)
    tinfo["manifest_url"] = manifest_url
    
    tinfo["tracks"] = tinfo.get("tracks", {})

    for track in title.tracks:
        track_str = str(track)
        track_data = tinfo["tracks"].setdefault(track_str, {})
        
        k_data = track_data.setdefault("keys", {})
        
        if track.encrypted:
            kid = track.kid.lower().replace("-", "") if track.kid else None
            if kid and kid in all_keys:
                k_data[kid] = all_keys[kid]
            elif track.key and kid:
                k_data[kid] = track.key.lower()
        else:
            if not k_data:
                k_data["null"] = "null"
                
        if isinstance(track, TextTrack):
            url = track.url[0] if isinstance(track.url, list) else track.url
            track_data["url"] = url

    export_path.write_text(json.dumps(doc, indent=4, ensure_ascii=False), encoding="utf-8")
```

### `wpgskd\config\__init__.py`

```python
import os
import sys
import logging
from types import SimpleNamespace
from pathlib import Path

import yaml
from appdirs import AppDirs
from requests.utils import CaseInsensitiveDict

from wpgskd.utils.collections import merge_dict

class Directories:
    def __init__(self):
        self.app_dirs = AppDirs("wpgskd", False)
        self.package_root = Path(__file__).resolve().parent.parent
        self.project_root = self.package_root.parent
        
        self.configuration = self.project_root / "config"
        self.user_configs = self.project_root
        
        self.service_configs = self.package_root / "servicookies"
        
        self.data = self.package_root
        
        self.downloads = self.project_root / "downloads"
        self.temp = self.project_root / "temp"
        self.cache = self.project_root / "cache"
        self.logs = self.project_root / "logs"
        self.exports = self.project_root / "exports"
        
        self.cookies = self.service_configs 

        self.devices = self.project_root / "devices"
        if not self.devices.exists():
            self.devices = self.package_root / "devices"

class Filenames:
    def __init__(self):
        self.log = os.path.join(directories.logs, "wpgskd_{time}.log")
        self.root_config = os.path.join(directories.package_root, "wpgskd.yml")
        self.user_root_config = os.path.join(directories.user_configs, "wpgskd.yml")
        
        self.service_config = os.path.join(directories.configuration, "services", "{service}.yml")
        self.user_service_config = os.path.join(directories.service_configs, "{service}.yml")
        
        self.subtitles = os.path.join(directories.temp, "TextTrack_{id}_{language_code}.srt")
        self.chapters = os.path.join(directories.temp, "{filename}_chapters.txt")

directories = Directories()
filenames = Filenames()

os.makedirs(directories.logs, exist_ok=True)
os.makedirs(directories.temp, exist_ok=True)
os.makedirs(directories.downloads, exist_ok=True)
os.makedirs(directories.cache, exist_ok=True)
os.makedirs(directories.exports, exist_ok=True)

config_data = {}
if os.path.exists(filenames.root_config):
    try:
        with open(filenames.root_config, encoding='utf-8') as fd:
            loaded = yaml.safe_load(fd)
            if loaded: config_data = loaded
    except Exception as e:
        print(f"Error loading config {filenames.root_config}: {e}")

user_config_data = {}
if os.path.exists(filenames.user_root_config):
    try:
        with open(filenames.user_root_config, encoding='utf-8') as fd:
            loaded = yaml.safe_load(fd)
            if loaded: user_config_data = loaded
    except Exception as e:
        print(f"Error loading user config {filenames.user_root_config}: {e}")

merge_dict(config_data, user_config_data)

if not config_data:
    print(f"Warning: No configuration loaded. Please ensure {filenames.root_config} exists.")

config = SimpleNamespace(**config_data)

credentials = getattr(config, 'credentials', {})

def setup_paths():
    if hasattr(config, 'directories'):
        downloads_path = config.directories.get('downloads')
        temp_path = config.directories.get('temp')

        if downloads_path:
            p = Path(downloads_path)
            if not p.is_absolute(): p = directories.project_root / p
            directories.downloads = p
            os.makedirs(directories.downloads, exist_ok=True)

        if temp_path:
            p = Path(temp_path)
            if not p.is_absolute(): p = directories.project_root / p
            directories.temp = p
            os.makedirs(directories.temp, exist_ok=True)
            
            filenames.subtitles = os.path.join(directories.temp, "TextTrack_{id}_{language_code}.srt")
            filenames.chapters = os.path.join(directories.temp, "{filename}_chapters.txt")

setup_paths()

try:
    from wpgskd.servicookies import SERVICE_MAP
except ImportError:
    SERVICE_MAP = {}

if not hasattr(config, 'arguments'):
    config.arguments = {}

if "range_" not in config.arguments:
    config.arguments["range_"] = config.arguments.get("range")

for service, aliases in SERVICE_MAP.items():
    for alias in aliases:
        config.arguments[alias] = config.arguments.get(service)

config.arguments = CaseInsensitiveDict(config.arguments)
```

### `wpgskd\config\wpgskd.yml`

```yaml
decrypter: 'packager'
tag: ''
tag_sd: ''

arguments: {}

aria2c:
  file_allocation: 'prealloc'

cdm:
  default: ''

credentials: {}

directories:
  temp: ''
  downloads: ''

headers:
  User-Agent: 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/142.0.0.0 Safari/537.36'

key_vaults:
  - type: 'local'
    name: 'Local'
    path: '{data_dir}/key_store.db'

output_template:
  movies: '{title}.{year}.{quality}.{source}.WEB-DL.{audio}.{video}-{tag}'
  series: '{title}.{season_episode}.{episode_name}.{quality}.{source}.WEB-DL.{audio}.{video}-{tag}'
  use_last_audio: false

profiles:
  default: 'default'
  
default_proxy_service: null  # Options: 'surfshark', 'nordvpn'

proxies: {}

nordvpn:
    #username: ''
    #password: ''

surfshark:
    #username: ''
    #password: ''
```

### `wpgskd\core\__init__.py`

```python

```

### `wpgskd\core\adobepass.py`

```python
import os
from abc import ABC

from yt_dlp import YoutubeDL
from yt_dlp.extractor.adobepass import AdobePassIE


class AdobePassVT(AdobePassIE, ABC):
    def __init__(self, credential, get_cache):
        super().__init__(
            YoutubeDL(
                {
                    "ap_mso": credential.extra,  # See yt_dlp.extractor.adobepass for supported MSO providers
                    "ap_username": credential.username,
                    "ap_password": credential.password,
                    "cachedir": os.path.realpath(get_cache("adobepass")),
                }
            )
        )
```

### `wpgskd\core\atomic_sql.py`

```python
import os
import sqlite3
import time
from threading import Lock

class AtomicSQL:
    """Race-condition and Threading safe SQL Database Interface."""
    def __init__(self):
        self.master_lock = Lock()
        self.db = {}
        self.cursor = {}
        self.session_lock = {}

    def load(self, connection: sqlite3.Connection):
        self.master_lock.acquire()
        try:
            session_id = None
            while not session_id or session_id in self.db:
                session_id = os.urandom(16)
            self.db[session_id] = connection
            self.cursor[session_id] = self.db[session_id].cursor()
            self.session_lock[session_id] = Lock()
            return session_id
        finally:
            self.master_lock.release()

    def safe_execute(self, session_id, action):
        if session_id not in self.db:
            raise ValueError(f"Session ID {session_id!r} is invalid.")
        self.master_lock.acquire()
        self.session_lock[session_id].acquire()
        try:
            failures = 0
            while True:
                try:
                    action(db=self.db[session_id], cursor=self.cursor[session_id])
                    break
                except sqlite3.OperationalError:
                    failures += 1
                    delay = 3 * failures
                    print(f"AtomicSQL.safe_execute failed, retrying in {delay} seconds...")
                    time.sleep(delay)
                if failures == 10:
                    raise ValueError("AtomicSQL.safe_execute failed too many time's. Aborting.")
            return self.cursor[session_id]
        finally:
            self.session_lock[session_id].release()
            self.master_lock.release()

    def commit(self, session_id):
        self.safe_execute(session_id, lambda db, cursor: db.commit())
        return True
```

### `wpgskd\core\base64.py`

```python
import base64


def encode(s):
    if isinstance(s, str):
        s = s.encode()
    return base64.b64encode(s).decode()


def decode(s):
    if isinstance(s, str):
        s = s.encode()
    return base64.b64decode(s + b"==")


def urlsafe_encode(s):
    if isinstance(s, str):
        s = s.encode()
    return base64.urlsafe_b64encode(s).decode().rstrip("=")


def urlsafe_decode(s):
    if isinstance(s, str):
        s = s.encode()
    return base64.urlsafe_b64decode(s + b"==")
```

### `wpgskd\core\collections.py`

```python
import itertools
from typing import Iterable, Sequence

class CaseInsensitiveDict(dict):
    """A dictionary with case-insensitive keys."""
    def __init__(self, *args, **kwargs):
        super().__init__(*args, **kwargs)
        for k in self.keys():
            if not isinstance(k, (str, bytes)):
                raise ValueError(f"dictionary keys must be str or bytes, not {type(k)}")

    def _resolve_key(self, key):
        if not isinstance(key, (str, bytes)):
            raise ValueError(f"dictionary keys must be str or bytes, not {type(key)}")
        return next((x for x in self.keys() if x.casefold() == key.casefold()), key)

    def __contains__(self, key): return super().__contains__(self._resolve_key(key))
    def __getitem__(self, key): return super().__getitem__(self._resolve_key(key))
    def __setitem__(self, key, value): return super().__setitem__(self._resolve_key(key), value)
    def get(self, key, default=None): return super().get(self._resolve_key(key), default)
    def pop(self, key): return super().pop(self._resolve_key(key))
    def setdefault(self, key, value=None): return super().setdefault(self._resolve_key(key), value)

def as_lists(*args):
    for item in args:
        yield item if isinstance(item, list) else [item]

def as_list(*args):
    if args == (None,): return []
    return list(itertools.chain.from_iterable(as_lists(*args)))

def first(iterable): return next(iter(iterable))
def first_or_else(iterable, default):
    item = next(iter(iterable or []), None)
    return default if item is None else item
def first_or_none(iterable): return first_or_else(iterable, None)

def flatten(items, ignore_types=str):
    if isinstance(items, (Iterable, Sequence)) and not isinstance(items, ignore_types):
        for i in items:
            yield from flatten(i, ignore_types)
    else:
        yield items

def merge_dict(*dicts):
    """Recursively merge dicts into dest in-place."""
    dest = dicts[0]
    for d in dicts[1:]:
        for key, value in d.items():
            if isinstance(value, dict):
                node = dest.setdefault(key, {})
                merge_dict(node, value)
            else:
                dest[key] = value
```

### `wpgskd\core\config.py`

```python
import logging
from pathlib import Path
from typing import Any, Optional, List
from dataclasses import dataclass, field

log = logging.getLogger("CoreConfig")

@dataclass
class CoreConfig:
    cdm_name: str = "default"
    decrypter: str = "packager"
    profile: str = "default"
    
    quality: Optional[Any] = None
    vcodec: str = "H264"
    acodec: Optional[str] = None
    vbitrate: Optional[int] = None
    abitrate: Optional[int] = None
    atmos: bool = False
    channels: Optional[str] = None
    range_: str = "SDR"
    wanted: Optional[List[str]] = None
    alang: List[str] = field(default_factory=lambda: ["orig"])
    slang: List[str] = field(default_factory=lambda: ["all"])
    
    audio_only: bool = False
    subs_only: bool = False
    chapters_only: bool = False
    no_subs: bool = False
    no_audio: bool = False
    no_video: bool = False
    no_chapters: bool = False
    audio_description: bool = False
    no_mux: bool = False
    mux: bool = False
    worst: bool = False
    sync_vat: bool = False
    no_sync_subs: bool = False
    
    use_cache: bool = True
    use_cdm: bool = True
    export: bool = False
    keys_only: bool = False
    
    temp_dir: Path = None
    out_dir: Path = None
    
    def apply_overrides(self, **kwargs):
        for key, value in kwargs.items():
            if value is not None and hasattr(self, key):
                setattr(self, key, value)
```

### `wpgskd\core\console.py`

```python
import logging
from typing import List, Any
from wpgskd.core.tracks.title import Title, Titles
from wpgskd.core.utilities import humanize_size, format_duration

log = logging.getLogger("Console")

class ConsoleUI:

    @staticmethod
    def print_titles(titles: Titles):
        if not titles:
            return

        is_tv = any(x.type == Title.Types.TV for x in titles)
        
        if is_tv:
            seasons = {}
            for t in titles:
                s = getattr(t, 'season', 0)
                seasons.setdefault(s, []).append(t)
                
            breakdown = ", ".join(f"S{s}({len(seasons[s])})" for s in sorted(seasons.keys()))
            log.info(f"{len(seasons)} seasons, {breakdown}")
        else:
            label = f"{len(titles)} Movie{['s', ''][len(titles) == 1]}"
            log.info(label)
            for m in titles:
                name = getattr(m, 'name', str(m))
                year = getattr(m, 'year', None)
                log.info(f"  {name} ({year or '?'})")
                
    @staticmethod
    def print_tracks(tracks: Any, title: Title = None):
        if not tracks:
            return

        for v in tracks.videos:
            codec = v.get_codec_display()
            
            range_str = "SDR"
            if getattr(v, 'dvhdr', False): range_str = "DV+HDR"
            elif getattr(v, 'dv', False): range_str = "DV"
            elif getattr(v, 'hdr10', False): range_str = "HDR10"
            elif getattr(v, 'hlg', False): range_str = "HLG"
            
            res_str = f"{v.width}x{v.height}"
            bitrate_str = f"{v.bitrate // 1000 if v.bitrate else '?'} kb/s"
            fps_str = f"{v.fps:.3f} FPS" if v.fps else "N/A"
            
            dur_sec = v.duration_seconds()
            size_bytes = v.size if v.size else v.computed_size_bytes()
            size_str = humanize_size(size_bytes) if size_bytes else "N/A"
            dur_str = format_duration(dur_sec) if dur_sec else "N/A"
                    
            enc_str = "Encrypted" if v.encrypted else "Unencrypted"
            
            log.info(f"├─ VID | {codec} | {range_str} | {res_str} | {bitrate_str} | {fps_str} | {size_str} | {dur_str} | {enc_str}")

        for a in tracks.audios:
            codec = a.get_codec_display()
            ch_str = a.channels or "?"
            bitrate_str = f"{a.bitrate // 1000 if a.bitrate else '?'} kb/s"
            lang_str = str(a.language)
            
            desc_str = " (Descriptive)" if a.descriptive else ""
            orig_str = " [Original]" if a.is_original_lang else ""
            
            dur_sec = a.duration_seconds()
            size_bytes = a.size if a.size else a.computed_size_bytes()
            size_str = humanize_size(size_bytes) if size_bytes else "N/A"
            dur_str = format_duration(dur_sec) if dur_sec else "N/A"
                    
            enc_str = "Encrypted" if a.encrypted else "Unencrypted"
            
            log.info(f"├─ AUD | {codec} | {ch_str} | {bitrate_str} | {lang_str}{orig_str}{desc_str} | {size_str} | {dur_str} | {enc_str}")

        for t in tracks.subtitles:
            codec = t.codec or "vtt"
            
            flags = []
            if t.is_original_lang: flags.append("orig")
            if t.forced: flags.append("Forced")
            if t.sdh: flags.append("SDH")
            if t.cc: flags.append("CC")
            flag_str = " ".join(flags)
            
            lang_str = str(t.language)
            
            parts = ["├─ SUB", codec, lang_str]
            if flag_str:
                parts.append(flag_str)
            log.info(" | ".join(parts))
```

### `wpgskd\core\constants.py`

```python
from enum import Enum

class EncryptionScheme(Enum):
    NONE = "none"
    WIDEVINE = "widevine"
    PLAYREADY = "playready"
    CLEARKEY = "clearkey"
    AES_128 = "aes-128"
    AES_128_ECB = "aes-128-ecb"
    SAMPLE_AES = "SAMPLE-AES"

LANGUAGE_MUX_MAP = {
    "none": "und",
    "nb": "nor",
}

TERRITORY_MAP = {
    "001": "",
    "150": "European",
    "419": "Latin American",
    "AU": "Australian",
    "BE": "Flemish",
    "BR": "Brazilian",
    "CA": "Canadian",
    "CZ": "",
    "CN": "Chinese Mainland",
    "DK": "",
    "EG": "Egyptian",
    "ES": "European",
    "FR": "European",
    "GB": "British",
    "GR": "",
    "HK": "Hong Kong",
    "IL": "",
    "IN": "",
    "JP": "Japan",
    "KR": "",
    "MY": "",
    "NO": "",
    "PH": "",
    "PS": "Palestinian",
    "PT": "European",
    "SE": "",
    "SY": "Syrian",
    "TW": "Taiwan",
    "US": "American",
}

LANGUAGE_MAX_DISTANCE = 5

CODEC_MAP = {
    "avc1": "H.264",
    "hev1": "H.265",
    "hvc1": "H.265",
    "dvh1": "H.265",
    "dvhe": "H.265",
    "av01": "AV1",
    "aac": "AAC",
    "mp4a": "AAC",
    "stereo": "AAC",
    "HE": "HE-AAC",
    "ac3": "AC3",
    "ac-3": "AC3",
    "dd": "DD",
    "eac": "E-AC3",
    "eac3": "E-AC3",
    "eac-3": "E-AC3",
    "ec-3": "DD+",
    "ddp": "DD+",
    "dd+": "DD+",
    "atmos": "DD+ Atmos",
    "ec3": "DD+",
    "srt": "SRT",
    "vtt": "VTT",
    "wvtt": "WVTT",
    "dfxp": "TTML",
    "stpp": "TTML",
    "ttml": "TTML",
    "tt": "TTML",
    "ass": "ASS",
    "ssa": "SSA",
}
```

### `wpgskd\core\credential.py`

```python
import hashlib
import re
from typing import Optional

import requests
import validators

class Credential:
    """Username (or Email) and Password Credential."""

    def __init__(self, username: str, password: str, extra: Optional[str] = None):
        self.username = username
        self.password = password
        self.extra = extra
        self.sha1 = hashlib.sha1(self.dumps().encode()).hexdigest()

    def __bool__(self):
        return bool(self.username) and bool(self.password)

    def __str__(self):
        return self.dumps()

    def __repr__(self):
        return "{name}({items})".format(
            name=self.__class__.__name__,
            items=", ".join([f"{k}={repr(v)}" for k, v in self.__dict__.items()])
        )

    def dumps(self) -> str:
        """Return credential data as a string."""
        return f"{self.username}:{self.password}" + (f":{self.extra}" if self.extra else "")

    def dump(self, path: str):
        """Write credential data to a file."""
        with open(path, "w", encoding="utf-8") as fd:
            fd.write(self.dumps())

    @classmethod
    def loads(cls, text: str) -> 'Credential':
        """
        Load credential from a text string.
        Format: {username}:{password}[:{extra}]
        """
        text = "".join([x.strip() for x in text.splitlines(keepends=False)]).strip()
        credential = re.fullmatch(r"^([^:]+?):([^:]+?)(?::(.+))?$", text)
        if credential:
            return cls(*credential.groups())
        raise ValueError("No credentials found in text string. Expecting the format `username:password`")

    @classmethod
    def load(cls, uri: str, session: Optional[requests.Session] = None) -> 'Credential':
        """
        Load Credential from a remote URL string or a local file path.
        """
        if validators.url(uri):
            return cls.loads((session or requests).get(uri).text)
        else:
            with open(uri, encoding="utf-8") as fd:
                return cls.loads(fd.read())
```

### `wpgskd\core\decryptor.py`

```python
import os
import sys
import re
import shutil
import logging
import subprocess
from typing import Optional, Dict, Any
from io import TextIOWrapper

from wpgskd.core.tracks.tracks import Track
from wpgskd.core.tracks.video import VideoTrack
from wpgskd.core.tracks.audio import AudioTrack

log = logging.getLogger("Decryptor")

class Decryptor:

    @staticmethod
    def find_executable(name: str) -> Optional[str]:
        if name == "packager":
            plat = {"win32": "win", "darwin": "osx"}.get(sys.platform, sys.platform)
            candidates = ["shaka-packager", "packager", f"packager-{plat}"]
            for c in candidates:
                path = shutil.which(c)
                if path: return path
            return None
        if name == "mp4decrypt":
            return shutil.which("mp4decrypt")
        return shutil.which(name)

    @staticmethod
    def decrypt(track: Track, keys: Dict[str, str], engine: str, temp_dir: str) -> Optional[str]:
        src = track.locate()
        if not src or not os.path.exists(src):
            log.error(f"Source file not found for decryption: {src}")
            return None

        dst = os.path.splitext(src)[0] + ".dec.mp4"
        
        if getattr(track, 'smooth', False) or getattr(track, 'encryption_scheme', None) == 'clearkey':
            engine = "mp4decrypt"

        if engine == "packager":
            dec = Decryptor._packager(track, keys, src, dst, temp_dir)
        elif engine == "mp4decrypt":
            dec = Decryptor._mp4decrypt(keys, src, dst)
        else:
            log.error(f"Unsupported decrypter engine: {engine}")
            return None

        return dec

    @staticmethod
    def _packager(track: Track, keys: Dict[str, str], src: str, dst: str, tmp: str) -> Optional[str]:
        exe = Decryptor.find_executable("packager")
        if not exe:
            raise FileNotFoundError("shaka-packager executable not found")

        stream = track.__class__.__name__.lower().replace("track", "")
        
        pk = track.kid.lower().replace("-", "")
        pv = keys.get(pk, next(iter(keys.values()), "")) if keys else ""
        
        if not pv:
            log.error("No valid key provided for shaka-packager")
            return None

        os.makedirs(tmp, exist_ok=True)
        
        cmd = [
            exe,
            f"input={src},stream={stream},output={dst}",
            "--enable_raw_key_decryption", "--keys",
            f"label=0:key_id={pk}:key={pv.lower()}, "
            f"label=1:key_id={'0' * 32}:key={pv.lower()}",
            "--temp_dir", tmp,
        ]

        proc = subprocess.Popen(cmd, stdout=subprocess.PIPE, stderr=subprocess.STDOUT, text=True)
        last = ""
        
        for line in proc.stdout:
            line = line.strip()
            if not line: continue
            
            if re.match(r"^\d+/\d+$", line):
                sys.stdout.write(f"\r   + Decrypting: {line}")
                sys.stdout.flush()
                last = line
            elif "Packaging completed successfully" in line:
                msg = f"{last} - Complete" if last else "Complete"
                sys.stdout.write(f"\r   + Decrypting: {msg}\n")
                sys.stdout.flush()
            elif any(w in line.lower() for w in ("error", "fail", "warning")):
                print(f"\n   ! {line}")
            elif line and not any(t in line for t in ("progress", "%", "[", "]")):
                print(f"\n   + {line}")
                
        proc.wait()
        
        if proc.returncode != 0:
            raise subprocess.CalledProcessError(proc.returncode, proc.args)
            
        return dst

    @staticmethod
    def _mp4decrypt(keys: Dict[str, str], src: str, dst: str) -> Optional[str]:
        exe = Decryptor.find_executable("mp4decrypt")
        if not exe:
            raise FileNotFoundError("mp4decrypt executable not found")

        cmd = [exe, "--show-progress"]
        
        for kid, key in keys.items():
            cmd.extend(["--key", f"{kid}:{key.lower()}"])
            
        cmd.extend([src, dst])

        proc = subprocess.Popen(cmd, stdout=subprocess.PIPE, stderr=subprocess.STDOUT, text=True)
        
        for line in proc.stdout:
            line = line.strip()
            if not line: continue
            
            if re.search(r"\d+%", line) or re.search(r"\d+/\d+", line):
                sys.stdout.write(f"\r   + Decrypting: {line}")
                sys.stdout.flush()
            elif "Progress" in line:
                continue
            elif any(w in line.lower() for w in ("error", "fail")):
                print(f"\n   ! {line}")
            else:
                print(f"   + {line}")
                
        proc.wait()
        
        if proc.returncode != 0:
            raise subprocess.CalledProcessError(proc.returncode, proc.args)
            
        return dst

    @staticmethod
    def repackage(path: str) -> bool:
        if not shutil.which("ffmpeg"):
            log.warning("FFmpeg not found, skipping repackage")
            return False

        fixed = f"{path}_fixed.mkv"
        try:
            proc = subprocess.Popen([
                "ffmpeg", "-hide_banner", "-loglevel", "error",
                "-i", path, "-map_metadata", "-1",
                "-fflags", "bitexact", "-codec", "copy", fixed,
            ], stderr=subprocess.PIPE, text=True)
            
            for line in proc.stderr:
                line = line.strip()
                if not line: continue
                if re.search(r"frame=\s*\d+", line):
                    sys.stdout.write(f"\r   + Repackaging: {line[:60]}")
                    sys.stdout.flush()
                elif "Insufficient bits" in line:
                    sys.stdout.write(f"\n   ! {line}\n   + Continuing...")
                    sys.stdout.flush()
                elif "error" in line.lower():
                    print(f"\n   ! {line}")
                    
            proc.wait()
            
            if proc.returncode == 0 and os.path.exists(fixed):
                sys.stdout.write("\r   + Repackaging: Complete\n")
                sys.stdout.flush()
                os.unlink(path)
                os.rename(fixed, path)
                return True
                
            sys.stdout.write("\n")
            log.warning(" - Repackage failed, keeping original file")
            if os.path.exists(fixed):
                os.unlink(fixed)
            return False
            
        except Exception as e:
            sys.stdout.write("\n")
            log.warning(f" - Repackage failed: {e}")
            if os.path.exists(fixed):
                os.unlink(fixed)
            return False
```

### `wpgskd\core\downloader.py`

```python
import re
import os
import sys
import shutil
import logging
import asyncio
import subprocess
from pathlib import Path
from typing import Optional, Any

import requests

from wpgskd.constants import EncryptionScheme
from wpgskd.core.tracks.tracks import Track
from wpgskd.core.io import aria2c, m3u8re

log = logging.getLogger("Downloader")

class Downloader:

    def __init__(self, session: requests.Session):
        self.session = session

    def download(self, track: Track, out_dir: str, name: str = None, headers: dict = None, 
                 proxy: str = None, title_ref: Any = None, all_keys: dict = None):

        if track.__class__.__name__ == "TextTrack" and isinstance(track.url, list):
            os.makedirs(out_dir, exist_ok=True)
            re_name = (name or "{type}_{id}_{enc}").format(
                type=track.__class__.__name__,
                id=track.id,
                enc="dec" if not track.encrypted else "enc"
            )
            save_path = os.path.join(out_dir, self._get_filename(track, re_name))
            self._download_and_merge_vtt(track.url, save_path, headers, proxy)
            track._location = save_path
            return

        if os.path.isfile(out_dir):
            raise ValueError("Path must be to a directory and not to a file")

        os.makedirs(out_dir, exist_ok=True)

        merged_headers = {}
        if headers:
            merged_headers.update(headers)
        if isinstance(getattr(track, 'extra', None), dict):
            track_headers = track.extra.get("headers")
            if isinstance(track_headers, dict):
                merged_headers.update(track_headers)
        headers = merged_headers or None

        re_name = (name or "{type}_{id}_{enc}").format(
            type=track.__class__.__name__,
            id=track.id,
            enc="enc" if track.encrypted else "dec"
        )

        if track.source.lower() == "abematv":
            self._download_abematv(track, out_dir, re_name)
            return

        if getattr(track, 'manifest_url', None) and getattr(track, 'mpd_representation_id', None):
            save_path = os.path.join(out_dir, self._get_filename(track, re_name))
            self._download_dash_manifest(track, save_path, headers, proxy)
            track._location = save_path
            return

        if track.descriptor == Track.Descriptor.ISM or getattr(track, 'smooth', False):
            self._download_ism(track, out_dir, re_name, headers, proxy)
            return

        if track.descriptor == Track.Descriptor.M3U and track.encryption_scheme == EncryptionScheme.AES_128:
            save_path = os.path.join(out_dir, self._get_filename(track, re_name))
            self._download_m3u8(track, save_path, headers, proxy)
            track._location = save_path
            return

        first_url = track.url[0] if isinstance(track.url, list) else track.url
        if track.descriptor == Track.Descriptor.M3U and isinstance(first_url, str) and ".m3u8" in first_url:
            save_path = os.path.join(out_dir, self._get_filename(track, re_name))
            self._download_m3u8(track, save_path, headers, proxy)
            track._location = save_path
            return

        if isinstance(track.url, list) and ".m3u8" in first_url:
            save_path = os.path.join(out_dir, self._get_filename(track, re_name))
            self._download_m3u8(track, save_path, headers, proxy)
            track._location = save_path
            return

        save_path = os.path.join(out_dir, self._get_filename(track, re_name))
        try:
            req_headers = headers if track.source not in ["ATVP", "iT"] else {}
            asyncio.run(aria2c(
                track.url, save_path,
                req_headers,
                proxy if track.needs_proxy else None
            ))
            track._location = save_path
        except (ValueError, subprocess.CalledProcessError) as e:
            dash_url = getattr(title_ref, 'dash_manifest_url', None) if title_ref else None
            if dash_url:
                log.warning(f"aria2c download failed. Attempting fallback with N_m3u8DL-RE...")
                try:
                    self._fallback_n_m3u8dl_re(track, dash_url, save_path, headers, proxy, all_keys)
                    track._location = save_path
                except Exception as fallback_e:
                    log.error(f"Fallback download with N_m3u8DL-RE also failed: {fallback_e}")
                    raise e
            else:
                raise e

    def _get_filename(self, track: Track, re_name: str) -> str:
        is_ass = hasattr(track, 'codec') and track.codec and track.codec.lower() in ['ass', 'ssa']

        if is_ass:
            return f"{re_name}.ass"
        elif track.__class__.__name__ == "TextTrack":
            ext = "vtt"
            if hasattr(track, 'codec') and track.codec:
                c = track.codec.lower()
                if c in ["ttml", "stpp", "dfxp"]:
                    ext = "ttml"
                elif c == "srt":
                    ext = "srt"
            return f"{re_name}.{ext}"
        elif track.__class__.__name__ == "AudioTrack" and track.source in ["iT", "ATVP", "TVer", "NHKPlus"]:
            return f"{re_name}.m4a"
        else:
            return f"{re_name}.mp4"

    def _download_and_merge_vtt(self, urls: list, save_path: str, headers: dict, proxy: str):
        log.info(f"Downloading and merging {len(urls)} subtitle segments...")
        merged_vtt = ""
        
        req_headers = headers if headers else {}
        
        proxies = None
        if proxy:
            proxies = {"http": proxy, "https": proxy}

        for i, url in enumerate(urls):
            try:
                res = self.session.get(url, headers=req_headers, proxies=proxies, timeout=30)
                res.raise_for_status()
                content = res.content.decode('utf-8', errors='ignore')
                
                lines = content.splitlines()
                current_vtt = ""
                for line in lines:
                    if line.strip() == "WEBVTT" and i > 0:
                        continue
                    if line.startswith("X-TIMESTAMP-MAP"):
                        continue
                    current_vtt += line + "\n"

                if i == 0:
                    merged_vtt = current_vtt
                else:
                    if current_vtt.startswith("\n"):
                        current_vtt = current_vtt[1:]
                    merged_vtt += current_vtt
                    
            except Exception as e:
                log.error(f" - Failed to download subtitle segment {i}: {e}")
                raise

        merged_vtt = re.sub(r'\n{3,}', '\n\n', merged_vtt).strip() + "\n"
        
        with open(save_path, "w", encoding="utf-8") as f:
            f.write(merged_vtt)   

    def _download_abematv(self, track: Track, out_dir: str, re_name: str):
        base_name = "VideoTrack_master_enc"
        muxed_location = os.path.join(out_dir, f"{base_name}.muxed.mkv")

        if os.path.exists(muxed_location):
            log.info(f"AbemaTV: Found pre-muxed file at {muxed_location}")
            track._location = muxed_location
            return

        video_path = os.path.join(out_dir, f"{base_name}.mp4")
        audio_path = os.path.join(out_dir, f"{base_name}.m4a")

        if os.path.exists(video_path) and os.path.exists(audio_path):
            log.info("Muxing AbemaTV tracks (RE output)...")
            cmd = [shutil.which("mkvmerge"), "-o", muxed_location, video_path, audio_path]
            subprocess.run(cmd, check=True, stdout=subprocess.DEVNULL)
            try:
                os.unlink(video_path)
                os.unlink(audio_path)
            except Exception:
                pass
            track._location = muxed_location
        elif os.path.exists(video_path):
            log.info("AbemaTV: Found single video file, using as muxed.")
            os.rename(video_path, muxed_location)
            track._location = muxed_location
        else:
            raise IOError("Missing RE output files for AbemaTV")

    def _download_m3u8(self, track: Track, save_path: str, headers: dict, proxy: str):
        log.info(f"Downloading HLS stream using N_m3u8DL-RE...")
        
        key = None
        if track.encryption_scheme == EncryptionScheme.AES_128:
            pass
        elif track.encryption_scheme == EncryptionScheme.CLEARKEY and track.key:
            key = f"{track.kid}:{track.key}"

        try:
            asyncio.run(m3u8re(
                track.url[0] if isinstance(track.url, list) else track.url,
                save_path,
                headers,
                proxy if track.needs_proxy else None,
                key=key
            ))
        except Exception as e:
            log.error(f"N_m3u8DL-RE failed: {e}")
            raise

    def _download_dash_manifest(self, track: Track, save_path: str, headers: dict, proxy: str):
        log.info(f"Downloading DASH manifest stream using N_m3u8DL-RE...")
        executable = shutil.which("N_m3u8DL-RE") or shutil.which("m3u8re")
        if not executable:
            raise EnvironmentError("N_m3u8DL-RE executable not found...")

        mpd_url = getattr(track, 'manifest_url', None)
        if not mpd_url:
            raise RuntimeError("MPD manifest URL missing for track")

        out_dir = Path(save_path).parent
        out_dir.mkdir(parents=True, exist_ok=True)

        cmd = [
            executable,
            mpd_url,
            "--save-name", Path(save_path).stem,
            "--save-dir", str(out_dir),
            "--tmp-dir", str(out_dir),
            "--auto-subtitle-fix", "False",
            "--log-level", "ERROR",
        ]

        if hasattr(track, "mpd_representation_id") and track.mpd_representation_id:
            cls_name = track.__class__.__name__
            if cls_name == "VideoTrack":
                cmd += ["--select-video", f"id={track.mpd_representation_id}"]
            elif cls_name == "AudioTrack":
                cmd += ["--select-audio", f"id={track.mpd_representation_id}"]
            elif cls_name == "TextTrack":
                cmd += ["--select-subtitle", f"id={track.mpd_representation_id}"]
        else:
            if track.__class__.__name__ == "TextTrack":
                cmd += ["--select-subtitle", f"lang={track.language}"]

        if track.needs_proxy and proxy:
            cmd += ["--custom-proxy", proxy]
        else:
            cmd += ["--use-system-proxy", "False"]

        if track.encryption_scheme == EncryptionScheme.CLEARKEY and getattr(track, 'key', None) and getattr(track, 'kid', None):
            cmd += ["--key", f"{track.kid}:{track.key}"]

        try:
            subprocess.run(cmd, check=True)
        except Exception as e:
            raise e

    def _download_ism(self, track: Track, out_dir: str, re_name: str, headers: dict, proxy: str):
        log.info(f"Downloading ISM stream using N_m3u8DL-RE...")
        executable = shutil.which("N_m3u8DL-RE") or shutil.which("m3u8re")
        if not executable:
            raise EnvironmentError("N_m3u8DL-RE executable not found...")

        first_url = track.url[0] if isinstance(track.url, list) else track.url
        ism_url = first_url.rsplit('/', 1)[0] + "/manifest"
        ism_url = ism_url.split('?')[0] 
        
        cmd = [
            executable,
            ism_url,
            "--save-name", re_name,
            "--save-dir", out_dir,
            "--tmp-dir", out_dir,
            "--auto-subtitle-fix", "True",
            "--log-level", "ERROR",
        ]
        
        if track.needs_proxy and proxy:
            cmd += ["--custom-proxy", proxy]
        else:
            cmd += ["--use-system-proxy", "False"]

        try:
            subprocess.run(cmd, check=True)
            files = list(Path(out_dir).glob(f"{re_name}*"))
            if files:
                track._location = str(files[0])
            else:
                raise IOError("ISM download produced no file")
        except Exception as e:
            raise e

    def _fallback_n_m3u8dl_re(self, track: Track, dash_manifest_url: str, save_path: str, headers: dict, proxy: str, all_keys: dict):
        executable = shutil.which("N_m3u8DL-RE") or shutil.which("m3u8re")
        if not executable:
            raise EnvironmentError("N_m3u8DL-RE executable not found...")

        cmd = [
            executable,
            dash_manifest_url,
            "--save-name", Path(save_path).stem,
            "--save-dir", str(Path(save_path).parent),
            "--tmp-dir", str(Path(save_path).parent),
            "--log-level", "INFO",
        ]

        if track.encrypted and all_keys and track.kid in all_keys:
            cmd.extend(["--key", f"{track.kid}:{all_keys[track.kid]}"])

        subprocess.run(cmd, check=True, capture_output=True, text=True)
```

### `wpgskd\core\events.py`

```python
import logging
from typing import Callable, Dict, List, Any

log = logging.getLogger("Events")

class EventManager:
    
    _listeners: Dict[str, List[Callable]] = {}

    @classmethod
    def subscribe(cls, event_name: str, callback: Callable):
        if event_name not in cls._listeners:
            cls._listeners[event_name] = []
        cls._listeners[event_name].append(callback)
        log.debug(f"Subscribed to event '{event_name}': {callback.__name__}")

    @classmethod
    def publish(cls, event_name: str, *args, **kwargs) -> Any:
        if event_name not in cls._listeners:
            return None
            
        for callback in cls._listeners[event_name]:
            try:
                result = callback(*args, **kwargs)
                if result is not None:
                    return result
            except Exception as e:
                log.error(f"Error in event listener for '{event_name}': {e}", exc_info=True)
                
        return None

class Events:
    BEFORE_DOWNLOAD = "before_download"
    AFTER_DOWNLOAD = "before_decrypt"
    AFTER_DECRYPT = "after_decrypt"
    BEFORE_MUX = "before_mux"
    AFTER_MUX = "after_mux"
```

### `wpgskd\core\io.py`

```python
import asyncio
import contextlib
import logging
import os
import re
import shutil
import subprocess
import sys
from pathlib import Path

import httpx
import pproxy
import requests
import yaml
import tqdm

log = logging.getLogger("io")

def load_yaml(path: str) -> dict:
    if not os.path.isfile(path):
        return {}
    with open(path) as fd:
        return yaml.safe_load(fd)

_ip_info = None

def get_ip_info(session=None, fresh=False) -> dict:
    """Use multiple services to get IP location information."""
    global _ip_info
    if fresh or not _ip_info:
        session = session or httpx
        try:
            resp = session.get("https://ipwho.is/").json()
            if resp.get("success") is not False:
                _ip_info = resp
                return _ip_info
        except Exception:
            pass
        try:
            resp = session.get("http://ip-api.com/json/").json()
            if "countryCode" in resp:
                _ip_info = {"country_code": resp["countryCode"]}
                return _ip_info
        except Exception:
            pass
        logging.getLogger("io").warning("Failed to get IP info. Assuming US.")
        _ip_info = {"country_code": "US"}
    return _ip_info

@contextlib.asynccontextmanager
async def start_pproxy(host, port, username, password):
    rerouted_proxy = "http://localhost:8081"
    server = pproxy.Server(rerouted_proxy)
    remote = pproxy.Connection(f"http+ssl://{host}:{port}#{username}:{password}")
    handler = await server.start_server(dict(rserver=[remote]))
    try:
        yield rerouted_proxy
    finally:
        handler.close()
        await handler.wait_closed()

async def aria2c(uri, out, headers=None, proxy=None):
    """Downloads file(s) using Aria2(c)."""
    executable = shutil.which("aria2c") or shutil.which("aria2")
    if not executable:
        raise EnvironmentError("Aria2c executable not found...")

    arguments = [
        executable, "-c", "--remote-time",
        "-o", os.path.basename(out),
        "-x", "16", "-j", "16", "-s", "16",
        "--allow-overwrite=true", "--auto-file-renaming=false",
        "--retry-wait", "5", "--max-tries", "15",
        "--max-file-not-found", "15", "--summary-interval", "0",
        "--file-allocation", "none" if sys.platform == "win32" else "falloc",
        "--console-log-level", "warn", "--download-result", "hide",
        "--user-agent", "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/138.0.0.0 Safari/537.36"
    ]

    for header, value in (headers or {}).items():
        if header.lower() == "accept-encoding": continue
        arguments.extend(["--header", f"{header}: {value}"])

    segmented = isinstance(uri, list)
    segments_dir = f"{out}_segments"

    if segmented:
        uri = "\n".join([
            f"{url}\n\tdir={segments_dir}\n\tout={i:08}.mp4"
            for i, url in enumerate(uri)
        ])

    if proxy:
        arguments.append("--all-proxy")
        if proxy.lower().startswith("https://"):
            auth, hostname = proxy[8:].split("@")
            async with start_pproxy(*hostname.split(":"), *auth.split(":")) as pproxy_:
                arguments.extend([pproxy_, "-d"])
                if segmented:
                    arguments.extend([segments_dir, "-i-"])
                    proc = await asyncio.create_subprocess_exec(*arguments, stdin=subprocess.PIPE)
                    await proc.communicate(uri.encode("utf-8"))
                else:
                    arguments.extend([os.path.dirname(out), uri])
                    proc = await asyncio.create_subprocess_exec(*arguments)
                    await proc.communicate()
        else:
            arguments.append(proxy)

    try:
        if segmented:
            subprocess.run(arguments + ["-d", segments_dir, "-i-"], input=uri, encoding="utf-8", check=True)
        else:
            subprocess.run(arguments + ["-d", os.path.dirname(out), uri], check=True)
    except subprocess.CalledProcessError:
        raise ValueError("Aria2c failed too many times, aborting")

    if segmented:
        with open(out, "wb") as ofd:
            for file in sorted(os.listdir(segments_dir)):
                file_path = os.path.join(segments_dir, file)
                with open(file_path, "rb") as ifd:
                    data = ifd.read()
                # Apple TV+ audio decryption fix
                data = re.sub(b"(tfhd\x00\x02\x00\x1a\x00\x00\x00\x01\x00\x00\x00)\x02", b"\\g<1>\x01", data)
                ofd.write(data)
                os.unlink(file)
        os.rmdir(segments_dir)

async def m3u8re(uri, out, headers=None, proxy=None, key=None):
    out = Path(out)
    if headers:
        headers.update({k: v for k, v in headers.items() if k.lower() != "accept-encoding"})

    executable = shutil.which("m3u8re") or shutil.which("N_m3u8DL-RE")
    if not executable:
        raise EnvironmentError("N_m3u8DL-RE executable not found...")

    if isinstance(uri, list):
        uri = uri[0]

    arguments = [
        executable, uri,
        "--tmp-dir", str(out.parent),
        "--save-dir", str(out.parent),
        "--save-name", out.name.replace('.mp4','').replace('.vtt','').replace('.m4a',''),
        "--auto-subtitle-fix", "False",
        "--thread-count", "32",
        "--log-level", "INFO"
    ]
    
    if key:
        arguments.extend(["--key", key])
        
    if headers:
        arguments.extend(["--header", "\r\n".join([f"{k}: {v}" for k, v in headers.items()])])
        
    if proxy:
        arguments.extend(["--custom-proxy", proxy])

    try:
        subprocess.run(arguments, check=True)
    except subprocess.CalledProcessError:
        raise ValueError("N_m3u8DL-RE failed too many times, aborting")

async def n_m3u8dl_re_dash(manifest_url, save_path, headers=None, proxy=None, track_id=None, kid_key_pairs=None):
    out = Path(save_path)
    executable = shutil.which("N_m3u8DL-RE") or shutil.which("m3u8re")
    if not executable:
        raise EnvironmentError("N_m3u8DL-RE executable was not found.")

    arguments = [
        executable, manifest_url,
        "--tmp-dir", str(out.parent), "--save-dir", str(out.parent),
        "--save-name", out.stem, "--log-level", "INFO",
        "--mux-after-done", "format=mkv",
    ]

    if headers:
        arguments.extend(["--header", "\r\n".join([f"{k}: {v}" for k, v in headers.items()])])

    if proxy:
        arguments.extend(["--custom-proxy", proxy])
    else:
        arguments.append("--no-proxy")

    if track_id:
        if 'video' in out.name.lower():
            arguments.extend(["-sv", f"id={track_id}", "-sa", "best"])
        elif 'audio' in out.name.lower():
            arguments.extend(["-sa", f"id={track_id}"])
    
    if kid_key_pairs:
        for kid, key in kid_key_pairs:
            arguments.extend(["--key", f"{kid}:{key}"])

    try:
        subprocess.run(arguments, check=True, capture_output=True, text=True, encoding='utf-8', errors='ignore')
    except subprocess.CalledProcessError as e:
        raise ValueError("N_m3u8DL-RE (fallback) failed, aborting")

    expected_mkv_path = out.with_suffix('.mkv')
    if expected_mkv_path.exists():
        if out.exists() and out.resolve() != expected_mkv_path.resolve():
            out.unlink()
        expected_mkv_path.rename(out)
    elif not out.exists():
        raise FileNotFoundError(f"N_m3u8DL-RE finished, but expected output file '{out}' was not found.")
```

### `wpgskd\core\muxer.py`

```python
import os
import re
import sys
import json
import time
import shutil
import logging
import subprocess
from pathlib import Path
from typing import Tuple, List, Optional
from io import TextIOWrapper

from wpgskd.config import directories, filenames
from wpgskd.core.tracks.tracks import Tracks, TextTrack
from wpgskd.core.tracks.title import Title
from wpgskd.core.utilities import is_close_match
from wpgskd.constants import LANGUAGE_MUX_MAP

log = logging.getLogger("Muxer")

class Muxer:

    @staticmethod
    def mux(title: Title, tracks: Tracks, no_sync_subs: bool = False) -> Tuple[str, int]:
        if not shutil.which("mkvmerge"):
            raise EnvironmentError("mkvmerge executable not found in PATH.")

        out_dir = Path(directories.downloads)
        if title.type == Title.Types.TV:
            out_dir = out_dir / title.parse_filename(folder=True)
        out_dir.mkdir(parents=True, exist_ok=True)

        muxed_location = out_dir / f"{title.parse_filename()}.muxed.mkv"
        
        if muxed_location.exists():
            muxed_location.unlink()

        cl = ["mkvmerge", "--output", str(muxed_location)]

        for i, vt in enumerate(tracks.videos):
            location = vt.locate()
            if not location:
                raise ValueError("A Video Track was not downloaded before muxing...")
            cl.extend([
                "--language", "0:und",
                "--disable-language-ietf",
                "--default-track", f"0:{i == 0}",
                "--compression", "0:none",
                "(", location, ")"
            ])

        for i, at in enumerate(tracks.audios):
            location = at.locate()
            if not location:
                raise ValueError("An Audio Track was not downloaded before muxing...")
            
            audio_display = at.get_codec_display()
            if at.atmos and "Atmos" not in audio_display:
                audio_display += " Atmos"

            cl.extend([
                "--track-name", f"0:{at.get_track_name() or audio_display}",
                "--language", f"0:{LANGUAGE_MUX_MAP.get(str(at.language), at.language.to_alpha3())}",
                "--disable-language-ietf",
                "--default-track", f"0:{i == 0}",
                "--compression", "0:none",
                "(", location, ")"
            ])

        subtitles_to_mux = tracks.subtitles if not no_sync_subs else []
        for st in subtitles_to_mux:
            location = st.locate()
            if not location:
                raise ValueError("A Text Track was not downloaded before muxing...")
            
            try:
                if os.path.getsize(location) < 6:
                    continue
            except Exception:
                continue

            try:
                with open(location, "r", encoding="utf-8", errors="ignore") as f:
                    head = f.read(512)
                if re.match(r"CHAPTER\d+=", head.strip(), re.IGNORECASE):
                    continue
            except Exception:
                pass

            default = bool(
                tracks.audios and is_close_match(st.language, [tracks.audios[0].language]) and st.forced
            )

            sub_cmd = [
                "--track-name", f"0:{st.get_track_name() or ''}",
                "--language", f"0:{LANGUAGE_MUX_MAP.get(str(st.language), st.language.to_alpha3())}",
                "--disable-language-ietf",
                "--sub-charset", "0:UTF-8",
                "--forced-track", f"0:{st.forced}",
                "--default-track", f"0:{default}",
                "--compression", "0:none",
            ]
            sub_cmd.extend(["(", location, ")"])
            cl.extend(sub_cmd)

        if tracks.chapters:
            chapters_file = filenames.chapters.format(filename=title.filename)
            tracks.export_chapters(chapters_file)
            cl.extend(["--chapters", chapters_file])

        log.info(f"Muxing tracks into {muxed_location.name}...")
        p = subprocess.Popen(cl, stdout=subprocess.PIPE, stderr=subprocess.STDOUT)
        in_progress = False
        
        for line in TextIOWrapper(p.stdout, encoding="utf-8"):
            if re.search(r"Using the (?:demultiplexer|output module) for the format", line):
                continue
            if line.startswith("Progress:"):
                in_progress = True
                sys.stdout.write("\r" + line.rstrip('\n'))
            else:
                if in_progress:
                    in_progress = False
                    sys.stdout.write("\n")
                sys.stdout.write(line)
                
        returncode = p.wait()
        return str(muxed_location), returncode

    @staticmethod
    def export_chapters(chapters: list, to_file: str = None) -> str:
        data = "\n".join(map(repr, chapters))
        if to_file:
            os.makedirs(os.path.dirname(to_file) or ".", exist_ok=True)
            with open(to_file, "w", encoding="utf-8") as fd:
                fd.write(data)
        return data

    @staticmethod
    def apply_sync(mkv_path: str):
        sync_log = logging.getLogger("SyncVAT")
        mkvmerge_path = shutil.which("mkvmerge")
        ffprobe_path = shutil.which("ffprobe")

        if not os.path.exists(mkv_path):
            sync_log.error(f"MKV file not found: {mkv_path}")
            return

        sync_log.info("Waiting 2 seconds for file IO...")
        time.sleep(2)

        output_path = os.path.splitext(mkv_path)[0] + ".synced.mkv"

        try:
            result = subprocess.run(
                [mkvmerge_path, "-J", mkv_path],
                stdout=subprocess.PIPE, stderr=subprocess.PIPE,
                text=True, errors="replace"
            )
            mkv_info = json.loads(result.stdout) if result.returncode == 0 else {}

            video_duration = None
            audio_tracks = []

            for track in mkv_info.get("tracks", []):
                track_type = track.get("type")
                properties = track.get("properties", {})
                track_id = track["id"]

                duration_sec = None
                if properties.get("tag_duration"):
                    try:
                        parts = properties["tag_duration"].split(":")
                        if len(parts) == 3:
                            duration_sec = float(parts[2]) + int(parts[1]) * 60 + int(parts[0]) * 3600
                    except Exception:
                        pass

                if duration_sec is None and properties.get("duration"):
                    try:
                        duration_sec = float(properties["duration"]) / 1e9
                    except Exception:
                        pass

                if track_type == "video":
                    if video_duration is None and duration_sec:
                        video_duration = duration_sec
                elif track_type == "audio":
                    if duration_sec:
                        audio_tracks.append({"id": track_id, "duration": duration_sec})

            if not video_duration and ffprobe_path:
                sync_log.info("Video duration missing in mkvmerge, probing with ffprobe...")
                try:
                    ff_cmd = [
                        ffprobe_path, "-v", "error",
                        "-select_streams", "v:0",
                        "-show_entries", "format=duration:stream=duration",
                        "-of", "default=noprint_wrappers=1:nokey=1",
                        mkv_path
                    ]
                    ff_res = subprocess.run(ff_cmd, stdout=subprocess.PIPE, stderr=subprocess.PIPE, text=True)

                    valid_durations = []
                    for line in ff_res.stdout.splitlines():
                        line = line.strip()
                        if line and line != 'N/A':
                            try:
                                valid_durations.append(float(line))
                            except ValueError:
                                pass

                    if valid_durations:
                        video_duration = max(valid_durations)
                except Exception as e:
                    sync_log.warning(f"FFprobe failed: {e}")

            if not video_duration:
                sync_log.warning("Could not determine Video Duration. Skipping Sync.")
                return

            sync_log.info(f"Video Duration: {video_duration:.4f}s")

            needs_sync = False
            cmd = [mkvmerge_path, "-o", output_path]

            count = 0
            for audio in audio_tracks:
                if audio["duration"] > video_duration + 0.1:
                    factor = video_duration / audio["duration"]
                    cmd.extend(["--sync", f"{audio['id']}:0,{factor:.9f}"])
                    sync_log.info(
                        f"Syncing Audio {audio['id']}: {audio['duration']:.4f}s -> "
                        f"{video_duration:.4f}s (Factor: {factor:.6f})"
                    )
                    needs_sync = True
                    count += 1

            if not needs_sync:
                sync_log.info("Audio duration matches video, no sync needed.")
                return

            cmd.append(mkv_path)

            sync_log.info(f"Re-muxing to fix {count} audio tracks...")
            subprocess.run(cmd, check=True, stdout=subprocess.DEVNULL, stderr=subprocess.PIPE)

            time.sleep(1)
            if os.path.exists(mkv_path):
                os.unlink(mkv_path)
            os.rename(output_path, mkv_path)
            sync_log.info("Sync completed successfully on final file.")

        except Exception as e:
            sync_log.error(f"SyncVAT Failed: {e}")
            if os.path.exists(output_path):
                try:
                    os.unlink(output_path)
                except Exception:
                    pass
```

### `wpgskd\core\regex.py`

```python
import re


def find(pattern, string, group=None):
    if group:
        m = re.search(pattern, string)
        if m:
            return m.group(group)
    else:
        return next(iter(re.findall(pattern, string)), None)
```

### `wpgskd\core\resolver.py`

```python
import logging
import traceback
from typing import Optional, Tuple, Dict, Any
from uuid import UUID

from wpgskd.core.cdm.loader import CdmProvider
from wpgskd.core.vaults import Vaults
from wpgskd.core.vault import InsertResult
from wpgskd.core.tracks.video import VideoTrack

try:
    from wpgskd.utils.monalisa import MonaLisa
    MONALISA_AVAILABLE = True
except ImportError:
    MONALISA_AVAILABLE = False
    MonaLisa = None

log = logging.getLogger("Resolver")

class KeyResolver:
    def __init__(self, vaults: Vaults, cdm_provider: CdmProvider, use_cache: bool = True, use_cdm: bool = True):
        self.vaults = vaults
        self.cdm_provider = cdm_provider
        self.use_cache = use_cache
        self.use_cdm = use_cdm
        self._license_cache = {}

    def resolve(self, track: Any, title: Any, service: Any, service_name: str, session: Any = None) -> Tuple[Optional[str], Dict[str, str]]:
        all_keys: Dict[str, str] = {}

        if MONALISA_AVAILABLE and getattr(track, 'monalisa', False) and getattr(track, 'key', None):
            log.info(f" + KEY: {track.key} (From MonaLisa)")
            if track.kid:
                all_keys[self._norm(track.kid)] = track.key
            return track.key, all_keys

        if self.use_cache and not getattr(track, 'key', None):
            track.key, vault_used = self.vaults.get(track.kid, title.id)
            if track.key:
                log.debug(f" + KEY: {track.key} (From {vault_used.name} Vault)")
                self._sync_vault(track.kid, track.key, title.id, service_name, vault_used)
                all_keys[self._norm(track.kid)] = track.key
                return track.key, all_keys
        if self.use_cdm and not getattr(track, 'key', None):
            try:
                content_keys = self._license(track, title, service, service_name, session)
                if content_keys:
                    all_keys.update(content_keys)
                    primary_key = self._match(track, content_keys, service_name)
                    if primary_key:
                        self._cache_all(content_keys, service_name, title.id)
                        return primary_key, all_keys
            except Exception as e:
                log.debug(traceback.format_exc())
                raise ValueError(f"CDM license error: {e}")

        return None, all_keys

    def _license(self, track: Any, title: Any, service: Any, service_name: str, session: Any) -> Optional[Dict[str, str]]:
        cdm = self.cdm_provider.cdm_instance
        
        if self.cdm_provider.cdm_instance.cdm_type == "playready":
            return self._pr_license(cdm, track, title, service)
            
        return self._wv_license(cdm, track, title, service, service_name)

    def _wv_license(self, cdm: Any, track: Any, title: Any, service: Any, service_name: str) -> Dict[str, str]:
        pssh_data = getattr(track, 'pssh', None)
        if not pssh_data:
            raise ValueError("Track missing PSSH for Widevine CDM")
            
        pssh_key = str(pssh_data)
        if pssh_key in self._license_cache:
            return self._license_cache[pssh_key]
            
        sid = cdm.open()
        try:
            challenge = cdm.get_license_challenge(sid, pssh_data, privacy_mode=True)
            license_res = service.license(
                challenge=challenge, 
                title=title, 
                track=track, 
                session_id=sid,
                drm_type="widevine"
            )
            cdm.parse_license(sid, license_res)
            
            keys_list = cdm.get_keys(sid)
            result = {}
            for k in keys_list:
                kid = self._norm(k.get('kid'))
                key = k.get('key')
                if kid and key and kid != "00" * 16:
                    result[kid] = key.lower()
            
            self._license_cache[pssh_key] = result
            return result
            
        except Exception as e:
            raise ValueError(f"Widevine license request failed: {e}")
        finally:
            cdm.close(sid)

    def _pr_license(self, cdm: Any, track: Any, title: Any, service: Any) -> Dict[str, str]:
        pr_pssh = getattr(track, 'pr_pssh', None)
        if not pr_pssh:
            raise ValueError("Track missing PR_PSSH for PlayReady CDM")
            
        pssh_key = str(pr_pssh)
        if pssh_key in self._license_cache:
            return self._license_cache[pssh_key]
            
        try:
            from pyplayready.system.pssh import PSSH as PRPSSH
            wrm = PRPSSH(pr_pssh).wrm_headers[0]
        except Exception:
            raise ValueError("Failed to parse WRM Header from PR_PSSH")

        sid = cdm.open()
        try:
            challenge = cdm.get_license_challenge(sid, wrm).encode('utf-8')
            license_res = service.license(
                challenge=challenge, 
                title=title, 
                track=track, 
                session_id=sid,
                drm_type="playready"
            )
            
            if isinstance(license_res, bytes):
                license_res = license_res.decode('utf-8', errors='ignore')
                
            try:
                cdm.parse_license(sid, license_res)
            except Exception as parse_e:
                log.error(f"Failed to parse PlayReady license. Response preview: {license_res[:500]}")
                raise parse_e
            
            keys_list = cdm.get_keys(sid)
            result = {}
            for k in keys_list:
                kid = self._norm(k.get('kid'))
                key = k.get('key')
                if kid and key and kid != "00" * 16:
                    result[kid] = key.lower()

            self._license_cache[pssh_key] = result
            return result
            
        except Exception as e:
            raise ValueError(f"PlayReady license request failed: {e}")
        finally:
            cdm.close(sid)
                        
    def _match(self, track: Any, keys: Dict[str, str], service_name: str) -> Optional[str]:
        target_kid = self._norm(track.kid) if track.kid else None
        
        filtered_keys = {k: v for k, v in keys.items() if k not in ("0" * 32, "b770d5b4bb6b594daf985845aae9aa5f")}
        if not filtered_keys:
            filtered_keys = keys
            
        if not filtered_keys:
            return None

        for kid, key in filtered_keys.items():
            log.debug(f" + {kid}:{key}")

        if target_kid and target_kid in filtered_keys:
            return filtered_keys[target_kid]

        if service_name == "YouTubeMovies" and isinstance(track, VideoTrack) and filtered_keys:
            real_kid = next(iter(filtered_keys))
            log.info(f" + YouTube mapping: virtual {track.kid} -> real {real_kid}")
            track.kid = real_kid
            return filtered_keys[real_kid]

        if not target_kid:
            log.warning(f" - Track has no KID, using fallback key")
        else:
            log.warning(f" - No exact KID match for {track.kid}")
            log.warning(f" - Available: {list(filtered_keys.keys())}")

        if filtered_keys:
            fallback_kid = next(iter(filtered_keys))
            log.info(f" + Using fallback key from KID: {fallback_kid[:8]}...")
            if not track.kid:
                track.kid = fallback_kid
            return filtered_keys[fallback_kid]

        log.warning(f" - No exact KID match for {track.kid}")
        log.warning(f" - Available: {list(filtered_keys.keys())}")

        if filtered_keys:
            fallback_kid = next(iter(filtered_keys))
            log.info(f" + Using fallback key from KID: {fallback_kid[:8]}...")
            return filtered_keys[fallback_kid]
            
        return None

    def _sync_vault(self, kid: str, key: str, title_id: str, service_name: str, source_vault: Any) -> None:
        for v in self.vaults.vaults:
            if v is source_vault:
                continue
            try:
                res = v.insert_key(self.vaults.service, kid, key, title_id, commit=True)
                if res == InsertResult.SUCCESS:
                    log.debug(f" + Cached to {v.name} vault")
            except Exception:
                pass

    def _cache_all(self, keys: Dict[str, str], service_name: str, title_id: str) -> None:
        for v in self.vaults.vaults:
            try:
                added, existed = 0, 0
                for kid, key in keys.items():
                    res = v.insert_key(self.vaults.service, kid, key, title_id, commit=False)
                    if res == InsertResult.SUCCESS:
                        added += 1
                    elif res == InsertResult.ALREADY_EXISTS:
                        existed += 1
                v.commit()
                if added > 0:
                    log.debug(f" + Cached {added}/{len(keys)} keys to {v.name}")
                if existed > 0 and added == 0:
                    log.debug(f" + {existed}/{len(keys)} keys already existed in {v.name}")
            except Exception:
                pass

    @staticmethod
    def _norm(kid: Any) -> str:
        if hasattr(kid, 'hex'):
            return kid.hex.lower()
        if isinstance(kid, UUID):
            return kid.hex.lower()
        return str(kid).replace("-", "").replace("_", "").lower()
```

### `wpgskd\core\services.py`

```python
import re
from typing import List

class Services:
    ALIASES = {
        "amzn": "amazon",
        "atvp": "appletvplus",
        "dsnp": "disneyplus",
        "hmax": "hbomax",
        "pmtp": "paramountplus",
        "ytbe": "youtube"
    }

    @classmethod
    def get_tag(cls, service_name: str) -> str:
        if not service_name:
            return "unknown"
            
        tag = service_name.lower()
        return cls.ALIASES.get(tag, tag)

    @classmethod
    def get_tags(cls, service_names: List[str]) -> List[str]:
        return [cls.get_tag(name) for name in service_names]
```

### `wpgskd\core\session.py`

```python
import logging
from typing import Optional, Dict, Any
import requests
from requests.adapters import HTTPAdapter
from urllib3.util.retry import Retry

log = logging.getLogger("Session")

class SessionBuilder:

    @staticmethod
    def build(
        headers: Optional[Dict[str, str]] = None,
        retries: int = 5,
        backoff_factor: int = 1,
        status_forcelist: Optional[list] = None,
        raise_on_error: bool = True
    ) -> requests.Session:
        if status_forcelist is None:
            status_forcelist = [429, 500, 502, 503, 504]

        session = requests.Session()
        
        retry_strategy = Retry(
            total=retries,
            backoff_factor=backoff_factor,
            status_forcelist=status_forcelist,
            allowed_methods=["GET", "POST", "PUT", "DELETE", "HEAD", "OPTIONS"]
        )
        
        adapter = HTTPAdapter(max_retries=retry_strategy)
        session.mount("https://", adapter)
        session.mount("http://", adapter)

        if headers:
            session.headers.update(headers)

        if raise_on_error:
            session.hooks = {
                "response": lambda r, *args, **kwargs: r.raise_for_status()
            }

        return session

    @staticmethod
    def build_hybrid(
        headers: Optional[Dict[str, str]] = None,
        impersonate: str = "chrome120",
        verify: bool = False
    ) -> Any:
        try:
            from curl_cffi import requests as curl_requests
            import requests as std_requests
        except ImportError:
            log.warning("curl_cffi is not installed. Falling back to standard requests.")
            return SessionBuilder.build(headers=headers)

        class HybridSession:
            def __init__(self, hdrs, imp, vfy):
                self.curl = curl_requests.Session(impersonate=imp, verify=vfy)
                self.std = std_requests.Session()
                
                if hdrs:
                    self.curl.headers.update(hdrs)
                    self.std.headers.update(hdrs)
                    
                self.headers = self.curl.headers
                self.cookies = self.curl.cookies
                self.proxies = {} 

            def _sync_std_session(self):
                for k, v in self.curl.headers.items():
                    self.std.headers[k] = v

            def get(self, url, **kwargs):
                if kwargs.get('stream'):
                    self._sync_std_session()
                    return self.std.get(url, **kwargs)
                return self.curl.get(url, **kwargs)

            def post(self, url, **kwargs):
                if kwargs.get('stream'):
                    self._sync_std_session()
                    return self.std.post(url, **kwargs)
                return self.curl.post(url, **kwargs)

            def put(self, url, **kwargs):
                return self.curl.put(url, **kwargs)
                
            def delete(self, url, **kwargs):
                return self.curl.delete(url, **kwargs)

            def __getattr__(self, name):
                return getattr(self.curl, name)

        return HybridSession(headers, impersonate, verify)
```

### `wpgskd\core\sslciphers.py`

```python
import ssl
from typing import Optional

from requests.adapters import HTTPAdapter


class SSLCiphers(HTTPAdapter):
    """
    Custom HTTP Adapter to change the TLS Cipher set and security requirements.

    Security Level may optionally be provided. A level above 0 must be used at all times.
    A list of Security Levels and their security is listed below. Usually 2 is used by default.
    Do not set the Security level via @SECLEVEL in the cipher list.

    Level 0:
        Everything is permitted. This retains compatibility with previous versions of OpenSSL.

    Level 1:
        The security level corresponds to a minimum of 80 bits of security. Any parameters
        offering below 80 bits of security are excluded. As a result RSA, DSA and DH keys
        shorter than 1024 bits and ECC keys shorter than 160 bits are prohibited. All export
        cipher suites are prohibited since they all offer less than 80 bits of security. SSL
        version 2 is prohibited. Any cipher suite using MD5 for the MAC is also prohibited.

    Level 2:
        Security level set to 112 bits of security. As a result RSA, DSA and DH keys shorter
        than 2048 bits and ECC keys shorter than 224 bits are prohibited. In addition to the
        level 1 exclusions any cipher suite using RC4 is also prohibited. SSL version 3 is
        also not allowed. Compression is disabled.

    Level 3:
        Security level set to 128 bits of security. As a result RSA, DSA and DH keys shorter
        than 3072 bits and ECC keys shorter than 256 bits are prohibited. In addition to the
        level 2 exclusions cipher suites not offering forward secrecy are prohibited. TLS
        versions below 1.1 are not permitted. Session tickets are disabled.

    Level 4:
        Security level set to 192 bits of security. As a result RSA, DSA and DH keys shorter
        than 7680 bits and ECC keys shorter than 384 bits are prohibited. Cipher suites using
        SHA1 for the MAC are prohibited. TLS versions below 1.2 are not permitted.

    Level 5:
        Security level set to 256 bits of security. As a result RSA, DSA and DH keys shorter
        than 15360 bits and ECC keys shorter than 512 bits are prohibited.
    """

    def __init__(self, cipher_list: Optional[str] = None, security_level: int = 0, *args, **kwargs):
        if cipher_list:
            if not isinstance(cipher_list, str):
                raise TypeError(f"Expected cipher_list to be a str, not {cipher_list!r}")
            if "@SECLEVEL" in cipher_list:
                raise ValueError("You must not specify the Security Level manually in the cipher list.")
        if not isinstance(security_level, int):
            raise TypeError(f"Expected security_level to be an int, not {security_level!r}")
        if security_level not in range(6):
            raise ValueError(f"The security_level must be a value between 0 and 5, not {security_level}")

        if not cipher_list:
            # cpython's default cipher list differs to Python-requests cipher list
            cipher_list = "DEFAULT"

        cipher_list += f":@SECLEVEL={security_level}"

        ctx = ssl.create_default_context()
        ctx.check_hostname = False  # For some reason this is needed to avoid a verification error
        ctx.set_ciphers(cipher_list)

        self._ssl_context = ctx
        super().__init__(*args, **kwargs)

    def init_poolmanager(self, *args, **kwargs):
        kwargs["ssl_context"] = self._ssl_context
        return super().init_poolmanager(*args, **kwargs)

    def proxy_manager_for(self, *args, **kwargs):
        kwargs["ssl_context"] = self._ssl_context
        return super().proxy_manager_for(*args, **kwargs)
```

### `wpgskd\core\subprocess_utils.py`

```python
import json
import subprocess


def ffprobe(uri):
    """Use ffprobe on the provided data to get stream information."""
    args = [
        "ffprobe",
        "-v", "quiet",
        "-of", "json",
        "-show_streams"
    ]
    if isinstance(uri, str):
        args.extend([
            "-f", "lavfi",
            "-i", "movie={}[out+subcc]".format(uri.replace("\\", '/').replace(":", "\\\\:"))
        ])
    elif isinstance(uri, bytes):
        args.append("pipe:")
    try:
        ff = subprocess.run(
            args,
            input=uri if isinstance(uri, bytes) else None,
            check=True,
            capture_output=True
        )
    except subprocess.CalledProcessError:
        return {}
    return json.loads(ff.stdout.decode("utf-8"))
```

### `wpgskd\core\utilities.py`

```python
import re
import base64
import logging
from typing import Optional, Any
from datetime import timedelta
from hashlib import md5

from langcodes import Language, closest_match

from wpgskd.core.constants import LANGUAGE_MAX_DISTANCE
from wpgskd.vendor.pymp4.parser import Box
from pywidevine.cdm import Cdm 
from pywidevine.license_protocol_pb2 import WidevinePsshData

log = logging.getLogger("Utilities")

def get_boxes(data: bytes, box_type: bytes, as_bytes: bool = False):
    """Scan a byte array for a wanted box, then parse and yield each find."""
    if not isinstance(data, (bytes, bytearray)):
        raise ValueError("data must be bytes")
    while True:
        try:
            index = data.index(box_type)
        except ValueError:
            break
        if index < 0:
            break
        if index > 4:
            index -= 4  # size is before box type and is 4 bytes long
        data = data[index:]
        try:
            box = Box.parse(data)
        except IOError:
            break
        if as_bytes:
            box = Box.build(box)
        yield box

def is_close_match(language: Any, languages: Any) -> bool:
    if not (language and languages and all(languages)):
        return False
    languages = list(map(str, [x for x in languages if x]))
    return closest_match(language, languages)[1] <= LANGUAGE_MAX_DISTANCE

def get_closest_match(language: Any, languages: Any) -> Optional[Language]:
    match, distance = closest_match(language, list(map(str, languages)))
    if distance > LANGUAGE_MAX_DISTANCE:
        return None
    return Language.get(match)

def numeric_quality(quality: Any) -> int:
    if not quality:
        return 0
    if quality == "SD":
        return 576
    return int(quality)

def try_get(obj: Any, func: callable) -> Any:
    try:
        return func(obj)
    except (AttributeError, IndexError, KeyError, TypeError):
        return None

def short_hash(input: Any) -> str:
    return base_encode(int(md5(str(input).encode()).hexdigest(), 16))

def base_encode(num: int) -> str:
    alphabet = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz"
    if num == 0:
        return alphabet[0]
    arr = []
    base = len(alphabet)
    while num:
        num, rem = divmod(num, base)
        arr.append(alphabet[rem])
    return "".join(reversed(arr))

def sanitize_filename(filename: str) -> str:
    if not filename:
        return "unknown"
        
    filename = filename.replace("/", " - ").replace("\\", " - ")
    filename = filename.replace(":", " - ")
    filename = re.sub(r'[\*\?\"\<\>\|]', "", filename)
    filename = filename.replace("&", " and ")
    filename = re.sub(r'\.+', ".", filename)      
    filename = re.sub(r'\s+\.', ".", filename)     
    filename = re.sub(r'\.\s+', ".", filename)     
    
    filename = filename.strip(". ")
    return filename

def pt_to_sec(pt_str: str) -> Optional[float]:
    if not pt_str:
        return None
        
    pt_str = pt_str.strip()
    if pt_str.startswith('P0Y0M0DT'):
        pt_str = pt_str.replace('P0Y0M0DT', 'PT')
    elif pt_str.startswith('P') and 'T' in pt_str:
        pt_str = 'PT' + pt_str.split('T', 1)[1]
    elif not pt_str.startswith('PT'):
        return None
        
    match = re.match(r'PT(?:(\d+(?:\.\d+)?)H)?(?:(\d+(?:\.\d+)?)M)?(?:(\d+(?:\.\d+)?)S)?', pt_str)
    if not match:
        return None
        
    h = float(match.group(1) or 0)
    m = float(match.group(2) or 0)
    s = float(match.group(3) or 0)
    return h * 3600 + m * 60 + s

def format_duration(seconds: float) -> str:
    if seconds is None:
        return "N/A"
    h = int(seconds // 3600)
    m = int((seconds % 3600) // 60)
    s = int(seconds % 60)
    if h > 0:
        return f"{h}h{m}m{s}s"
    elif m > 0:
        return f"{m}m{s}s"
    else:
        return f"{s}s"

def get_track_size_estimate(bitrate: int, duration_sec: float) -> Optional[int]:
    if not bitrate or not duration_sec or duration_sec <= 0:
        return None
    return int((float(bitrate) * float(duration_sec)) / 8.0)

def humanize_size(num_bytes: int) -> str:
    try:
        size = float(num_bytes)
    except TypeError:
        return "N/A"
    units = ["B", "KB", "MB", "GB", "TB"]
    i = 0
    while size >= 1024 and i < len(units) - 1:
        size /= 1024.0
        i += 1
    return f"{size:.2f} {units[i]}"
```

### `wpgskd\core\vault.py`

```python
import logging
import sqlite3
import os
from abc import ABC, abstractmethod
from enum import Enum
from typing import Optional

import requests

from wpgskd.core.atomic_sql import AtomicSQL

log = logging.getLogger("Vault")


class InsertResult(Enum):
    FAILURE = 0
    SUCCESS = 1
    ALREADY_EXISTS = 2


class BaseVault(ABC):
    def __init__(self, name: str):
        self.name = name

    @abstractmethod
    def get_key(self, table: str, kid: str, title_id: str = "") -> Optional[str]:
        pass

    @abstractmethod
    def insert_key(self, table: str, kid: str, key: str, title: str = "", commit: bool = True) -> InsertResult:
        pass

    def create_table(self, table: str):
        pass

    def commit(self):
        pass


class LocalVault(BaseVault):
    def __init__(self, name: str, path: str, **kwargs):
        super().__init__(name)
        from wpgskd.config import directories 
        db_path = path.format(data_dir=directories.data)
        os.makedirs(os.path.dirname(db_path), exist_ok=True)
        
        self.con = sqlite3.connect(db_path)
        self.adb = AtomicSQL()
        self.ticket = self.adb.load(self.con)

    def table_exists(self, table: str) -> bool:
        r = self.adb.safe_execute(self.ticket, lambda db, cursor: cursor.execute(
            "SELECT count(name) FROM sqlite_master WHERE type='table' AND name=?", [table]
        )).fetchone()
        return r[0] == 1

    def create_table(self, table: str):
        if not self.table_exists(table):
            self.adb.safe_execute(self.ticket, lambda db, cursor: cursor.execute(
                f"""CREATE TABLE `{table}` (
                    "id" INTEGER NOT NULL UNIQUE,
                    "kid" TEXT NOT NULL COLLATE NOCASE,
                    "key_" TEXT NOT NULL COLLATE NOCASE,
                    "title" TEXT,
                    PRIMARY KEY("id" AUTOINCREMENT),
                    UNIQUE("kid", "key_")
                );"""
            ))
            self.adb.commit(self.ticket)

    def get_key(self, table: str, kid: str, title_id: str = "") -> Optional[str]:
        if not self.table_exists(table):
            return None
        r = self.adb.safe_execute(self.ticket, lambda db, cursor: cursor.execute(
            f"SELECT `key_` FROM `{table}` WHERE `kid`=?", [kid]
        )).fetchone()
        return r[0] if r else None

    def insert_key(self, table: str, kid: str, key: str, title: str = "", commit: bool = True) -> InsertResult:
        self.create_table(table)
        exists = self.adb.safe_execute(self.ticket, lambda db, cursor: cursor.execute(
            f"SELECT `id` FROM `{table}` WHERE `kid`=? AND `key_`=?", [kid, key]
        )).fetchone()
        if exists:
            return InsertResult.ALREADY_EXISTS
        
        self.adb.safe_execute(self.ticket, lambda db, cursor: cursor.execute(
            f"INSERT INTO `{table}` (kid, key_, title) VALUES (?, ?, ?)", (kid, key, title)
        ))
        if commit:
            self.adb.commit(self.ticket)
        return InsertResult.SUCCESS

    def commit(self):
        self.adb.commit(self.ticket)

class HTTPAPIVault(BaseVault):
    def __init__(self, name: str, host: str, password: str, **kwargs):
        super().__init__(name)
        self.url = host if host.endswith('/') else host + '/'
        self.password = password

    def get_key(self, table: str, kid: str, title_id: str = "") -> Optional[str]:
        payload = {
            "method": "GetKey", 
            "params": {"kid": kid, "service": table, "title": title_id}, 
            "token": self.password
        }
        try:
            res = requests.post(self.url, json=payload).json()
            keys = res.get("keys", [])
            if keys:
                return keys[0].get("key")
        except Exception as e:
            log.error(f"HTTPAPI Vault get failed: {e}")
        return None

    def insert_key(self, table: str, kid: str, key: str, title: str = "", commit: bool = True) -> InsertResult:
        payload = {
            "method": "InsertKey", 
            "params": {"kid": kid, "key": key, "service": table, "title": title}, 
            "token": self.password
        }
        try:
            res = requests.post(self.url, json=payload).json()
            if res.get("inserted"):
                return InsertResult.SUCCESS
            return InsertResult.ALREADY_EXISTS
        except Exception as e:
            log.error(f"HTTPAPI Vault insert failed: {e}")
            return InsertResult.FAILURE
```

### `wpgskd\core\vaults.py`

```python
import logging
from typing import Optional, Tuple, List, Type

from wpgskd.core.vault import BaseVault, LocalVault, HTTPAPIVault

log = logging.getLogger("Vaults")

class Vaults:    
    VAULT_TYPES = {
        "local": LocalVault,
        "httpapi": HTTPAPIVault,
    }

    def __init__(self, vaults_list: list, service: str):
        self.vaults: List[BaseVault] = []
        self.service = service.lower()
        
        for v in vaults_list:
            try:
                if isinstance(v, BaseVault):
                    vault = v
                else:
                    v_type = v.get("type", "").lower()
                    v_name = v.get("name", v_type)
                    vault_cls = self.VAULT_TYPES.get(v_type)
                    if not vault_cls:
                        log.warning(f"Unsupported vault type '{v_type}' for '{v_name}', skipping.")
                        continue
                    
                    cfg_copy = {k: val for k, val in v.items() if k not in ["type", "name"]}
                    vault = vault_cls(name=v_name, **cfg_copy)
                
                if isinstance(vault, LocalVault):
                    vault.create_table(self.service)
                    
                self.vaults.append(vault)
            except Exception as e:
                v_name = v.name if isinstance(v, BaseVault) else v.get('name')
                log.error(f"Failed to init vault {v_name}: {e}")
        
        self.vaults.sort(key=lambda v: 0 if isinstance(v, LocalVault) else 1)

    def get(self, kid: str, title_id: str = "") -> Tuple[Optional[str], Optional[BaseVault]]:
        for v in self.vaults:
            key = v.get_key(self.service, kid, title_id)
            if key:
                log.debug(f"Key {kid} found in vault {v.name}")
                return key, v
        return None, None

    def insert(self, kid: str, key: str, title_id: str = "") -> None:
        for v in self.vaults:
            try:
                res = v.insert_key(self.service, kid, key, title_id)
                if res.name == "SUCCESS":
                    log.debug(f"Inserted key to vault {v.name}")
            except Exception as e:
                log.warning(f"Failed to insert key to vault {v.name}: {e}")

    @staticmethod
    def load_vault(vault_cfg: dict) -> BaseVault:
        v_type = vault_cfg.get("type", "").lower()
        v_name = vault_cfg.get("name", v_type)
        no_push = vault_cfg.get("no_push", False)
        
        cfg_copy = {k: v for k, v in vault_cfg.items() if k not in ["type", "name", "no_push"]}
        
        vault_cls = Vaults.VAULT_TYPES.get(v_type)
        if not vault_cls:
            raise ValueError(f"Unknown vault type: {v_type}")
            
        return vault_cls(name=v_name, **cfg_copy)
```

### `wpgskd\core\xml.py`

```python
from lxml import etree

def load_xml(xml):
    if not isinstance(xml, bytes):
        xml = xml.encode("utf-8")
    root = etree.fromstring(xml)
    for elem in root.getiterator():
        if not hasattr(elem.tag, "find"):
            continue
        elem.tag = etree.QName(elem).localname
    etree.cleanup_namespaces(root)
    return root
```

### `wpgskd\core\bamsdk\__init__.py`

```python
# flake8: noqa
from wpgskd.core.bamsdk.bamsdk import BamSdk
```

### `wpgskd\core\bamsdk\bamsdk.py`

```python
import requests

from wpgskd.core.bamsdk.services.account import account
from wpgskd.core.bamsdk.services.bamIdentity import bamIdentity
from wpgskd.core.bamsdk.services.content import content
from wpgskd.core.bamsdk.services.device import device
from wpgskd.core.bamsdk.services.drm import drm
from wpgskd.core.bamsdk.services.media import media
from wpgskd.core.bamsdk.services.session import session
from wpgskd.core.bamsdk.services.token import token


class BamSdk:
    def __init__(self, endpoint, session_=None):
        self._session = session_ or requests.Session()

        self.config = self._session.get(endpoint).json()
        self.application = self.config["application"]
        self.commonHeaders = self.config["commonHeaders"]

        self.account = account(self.config["services"]["account"], self._session)
        self.bamIdentity = bamIdentity(self.config["services"]["bamIdentity"], self._session)
        self.content = content(self.config["services"]["content"], self._session)
        self.device = device(self.config["services"]["device"], self._session)
        self.drm = drm(self.config["services"]["drm"], self._session)
        self.media = media(self.config["services"]["media"], self._session)
        self.session = session(self.config["services"]["session"], self._session)
        self.token = token(self.config["services"]["token"], self._session)
```

### `wpgskd\core\bamsdk\services\__init__.py`

```python
import requests


class Service:
    def __init__(self, cfg, session=None):
        self.session = session or requests.Session()
        self.client = Client(cfg.get("client") or {})
        self.disabled = cfg.get("disabled")
        self.extras = cfg.get("extras")


class Client:
    def __init__(self, data):
        self.baseUrl = data.get("baseUrl")
        self.endpoints = {k: Endpoint(v) for k, v in (data.get("endpoints") or {}).items()}
        self.extras = data.get("extras") or {}


class Endpoint:
    def __init__(self, data):
        self.headers = data.get("headers") or {}
        self.href = data["href"]
        self.method = data.get("method") or "GET"
        self.templated = data.get("templated") or False
        self.timeout = data.get("timeout") or 15
        self.ttl = data.get("ttl") or 0

    # noinspection PyPep8Naming
    def get_headers(self, accessToken=None, apiKey=None):
        token = None
        if accessToken:
            token = {"accessToken": accessToken}
        elif apiKey:
            token = {"apiKey": apiKey}
        if token:
            self.headers.update({"Authorization": self.headers["Authorization"].format(**token)})
        return self.headers
```

### `wpgskd\core\bamsdk\services\account.py`

```python
from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class account(Service):
    def createAccountGrant(self, json: dict, access_token: str) -> dict:
        endpoint = self.client.endpoints["createAccountGrant"]
        return self.session.request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(accessToken=access_token),
            json=json,
        ).json()

    def getUserProfiles(self, access_token: str) -> dict:
        endpoint = self.client.endpoints["getCurrentAccount"]
        return self.session.request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(accessToken=access_token),
        ).json()

    def setActiveUserProfile(self, profile_id: str, access_token: str) -> dict:
        # Hardcoded since its not in v4 anymore
        return self.session.put(
            url=f"https://disney.api.edge.bamgrid.com/accounts/me/active-profile/{profile_id}",
            headers={"Authorization": f"Bearer {access_token}"},
        ).json()
```

### `wpgskd\core\bamsdk\services\bamIdentity.py`

```python
from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class bamIdentity(Service):
    def identityLogin(self, email, password, access_token):
        endpoint = self.client.endpoints["identityLogin"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(accessToken=access_token),
            json={
                "email": email,
                "password": password
            }
        ).prepare()
        res = self.session.send(req)
        return res.json()
```

### `wpgskd\core\bamsdk\services\content.py`

```python
from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class content(Service):
    def getDmcEpisodes(self, region, season_id, page, access_token):
        endpoint = self.client.endpoints["getDmcEpisodes"]
        req = Request(
            method=endpoint.method,
            url=f"https://disney.content.edge.bamgrid.com/svc/content/DmcEpisodes/version/5.1/region/{region}/audience/false/maturity/1850/language/en/seasonId/{season_id}/pageSize/15/page/{page}",
            headers=endpoint.get_headers(accessToken=access_token)
        ).prepare()
        res = self.session.send(req)
        return res.json()

    def getDmcSeriesBundle(self, region, media_id, access_token):
        endpoint = self.client.endpoints["getDmcSeriesBundle"]
        req = Request(
            method=endpoint.method,
            url=f"https://disney.content.edge.bamgrid.com/svc/content/DmcSeriesBundle/version/5.1/region/{region}/audience/false/maturity/1850/language/en/encodedSeriesId//{media_id}",
            headers=endpoint.get_headers(accessToken=access_token)
        ).prepare()
        res = self.session.send(req)
        return res.json()

    def getDmcVideoBundle(self, region, media_id, access_token):
        endpoint = self.client.endpoints["getDmcVideoBundle"]
        req = Request(
            method=endpoint.method,
            url=f"https://disney.content.edge.bamgrid.com/svc/content/DmcVideoBundle/version/5.1/region/{region}/audience/false/maturity/1850/language/en/encodedFamilyId/{media_id}",
            headers=endpoint.get_headers(accessToken=access_token)
        ).prepare()
        res = self.session.send(req)
        return res.json()
```

### `wpgskd\core\bamsdk\services\device.py`

```python
from json import JSONDecodeError

from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class device(Service):

    def createDeviceGrant(self, json, api_key):
        endpoint = self.client.endpoints["createDeviceGrant"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(apiKey=api_key),
            json=json
        ).prepare()
        res = self.session.send(req)
        try:
            data = res.json()
        except JSONDecodeError:
            raise Exception(f"An unexpected response occurred for bamsdk.createDeviceGrant: {res.text}")
        return data
```

### `wpgskd\core\bamsdk\services\drm.py`

```python
import json

from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class drm(Service):
    def widevineCertificate(self):
        endpoint = self.client.endpoints["widevineCertificate"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.headers
        ).prepare()
        res = self.session.send(req)
        return res.content

    def widevineLicense(self, licence, access_token):
        endpoint = self.client.endpoints["widevineLicense"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(accessToken=access_token),
            data=licence
        ).prepare()
        res = self.session.send(req)
        try:
            # if it's json content, then an error occurred
            res = json.loads(res.text)
            raise Exception(f"Failed to obtain license: {res}")
        except json.JSONDecodeError:
            return res.content
    
    def playreadyLicense(self, licence, access_token):
        endpoint = self.client.endpoints["playReadyLicense"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(accessToken=access_token),
            data=licence
        ).prepare()
        res = self.session.send(req)
        try:
            # if it's json content, then an error occurred
            res = json.loads(res.text)
            raise Exception(f"Failed to obtain license: {res}")
        except json.JSONDecodeError:
            return res.content
```

### `wpgskd\core\bamsdk\services\media.py`

```python
from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class media(Service):
    def __init__(self, cfg, session=None):
        super().__init__(cfg, session)
        self.uhd_allowed = self.extras["isUhdAllowed"]
        self.default_scenario = self.extras["playbackScenarioDefault"]
        self.scenarios = self.extras["playbackScenarios"]
        self.restricted_scenario = self.extras["restrictedPlaybackScenario"]
        self.security_requirements = self.extras["securityCheckRequirements"]

    def mediaPayload(self, media_id, scenario, access_token):
        endpoint = self.client.endpoints["mediaPayload"]
        req = Request(
            method=endpoint.method,
            url=f"{self.client.baseUrl}/media/{media_id}/scenarios/{scenario}",
            headers=endpoint.get_headers(accessToken=access_token)
        ).prepare()
        res = self.session.send(req)
        return res.json()
```

### `wpgskd\core\bamsdk\services\session.py`

```python
from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class session(Service):
    def getInfo(self, access_token):
        endpoint = self.client.endpoints["getInfo"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(accessToken=access_token)
        ).prepare()
        res = self.session.send(req)
        return res.json()

    def getLocation(self, access_token):
        endpoint = self.client.endpoints["getLocation"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(accessToken=access_token)
        ).prepare()
        res = self.session.send(req)
        return res.json()
```

### `wpgskd\core\bamsdk\services\token.py`

```python
from requests import Request

from wpgskd.core.bamsdk.services import Service


# noinspection PyPep8Naming
class token(Service):
    def __init__(self, cfg, session=None):
        super().__init__(cfg, session)
        self.subject_tokens = self.extras["subjectTokenTypes"]

    def exchange(self, data, api_key):
        endpoint = self.client.endpoints["exchange"]
        req = Request(
            method=endpoint.method,
            url=endpoint.href,
            headers=endpoint.get_headers(apiKey=api_key),
            data=data
        ).prepare()
        res = self.session.send(req)
        return res.json()
```

### `wpgskd\core\cdm\__init__.py`

```python

```

### `wpgskd\core\cdm\base.py`

```python
from abc import ABC, abstractmethod
from typing import List, Optional, Union
from uuid import UUID

class BaseCdm(ABC):
    
    @property
    @abstractmethod
    def security_level(self) -> int:
        pass

    @property
    @abstractmethod
    def system_id(self) -> int:
        pass

    @property
    @abstractmethod
    def cdm_type(self) -> str:
        pass

    @abstractmethod
    def open(self) -> bytes:
        pass

    @abstractmethod
    def close(self, session_id: bytes) -> None:
        pass

    @abstractmethod
    def get_license_challenge(self, session_id: bytes, pssh_data: Union[str, bytes], privacy_mode: bool = True) -> bytes:
        pass

    @abstractmethod
    def parse_license(self, session_id: bytes, license_message: Union[str, bytes]) -> None:
        pass

    @abstractmethod
    def get_keys(self, session_id: bytes, key_type: Optional[str] = None) -> List[dict]:
        pass
```

### `wpgskd\core\cdm\custom_remote_cdm.py`

```python
import logging
import base64
import requests
from typing import List, Optional, Union, Dict, Any
from wpgskd.core.cdm.base import BaseCdm

log = logging.getLogger("RemoteCDM")

class RemoteCdmAdapter(BaseCdm):
    def __init__(self, api_config: Dict[str, Any]):
        self.host = api_config["host"]
        self.key = api_config["key"]
        self.device_name = api_config["device"]
        self._security_level = int(api_config.get("security_level", 3))
        self._system_id = int(api_config.get("system_id", 0))
        self._cdm_type = api_config.get("type", "widevine").lower()
        self.session = requests.Session()
        self.session.headers.update({"X-Secret-Key": self.key})

    @property
    def security_level(self): return self._security_level
    @property
    def system_id(self): return self._system_id
    @property
    def cdm_type(self): return self._cdm_type

    def open(self) -> bytes:
        r = self.session.get(f"{self.host}/{self.device_name}/open").json()
        if r['status'] != 200: raise ValueError(r['message'])
        return bytes.fromhex(r["data"]["session_id"])

    def close(self, session_id: bytes) -> None:
        self.session.get(f"{self.host}/{self.device_name}/close/{session_id.hex()}")

    def get_license_challenge(self, session_id: bytes, pssh_data: Union[str, bytes], privacy_mode: bool = True) -> bytes:
        if isinstance(pssh_data, bytes):
            pssh_data = base64.b64encode(pssh_data).decode()
        
        payload = {
            "session_id": session_id.hex(),
            "init_data": pssh_data,
            "privacy_mode": privacy_mode
        }
        r = self.session.post(f"{self.host}/{self.device_name}/get_license_challenge", json=payload).json()
        if r['status'] != 200: raise ValueError(r['message'])
        return base64.b64decode(r["data"]["challenge_b64"])

    def parse_license(self, session_id: bytes, license_message: Union[str, bytes]) -> None:
        if isinstance(license_message, bytes):
            license_message = base64.b64encode(license_message).decode()
            
        payload = {
            "session_id": session_id.hex(),
            "license_message": license_message
        }
        r = self.session.post(f"{self.host}/{self.device_name}/parse_license", json=payload).json()
        if r['status'] != 200: raise ValueError(r['message'])

    def get_keys(self, session_id: bytes, key_type: Optional[str] = None) -> List[dict]:
        payload = {"session_id": session_id.hex()}
        r = self.session.post(f"{self.host}/{self.device_name}/get_keys", json=payload).json()
        if r['status'] != 200: raise ValueError(r['message'])
        
        keys = r["data"]["keys"]
        if key_type:
            return [k for k in keys if k.get("type") == key_type]
        return keys
```

### `wpgskd\core\cdm\detect.py`

```python
from pathlib import Path
import logging

log = logging.getLogger("CDMDetect")

def detect_cdm_type(path: Path) -> str:
    try:
        with open(path, "rb") as f:
            header = f.read(3)
        
        if header == b"WVD":
            return "widevine"
        elif header == b"PRD":
            return "playready"
        else:
            raise ValueError(f"Unknown CDM file header: {header}")
    except Exception as e:
        log.error(f"Failed to detect CDM type for {path}: {e}")
        raise
```

### `wpgskd\core\cdm\loader.py`

```python
import json
import time
import logging
from pathlib import Path
from typing import Optional, Dict, Any
from datetime import datetime, timedelta
from Crypto.Random import get_random_bytes

from wpgskd.core.cdm.base import BaseCdm
from wpgskd.core.cdm.detect import detect_cdm_type

log = logging.getLogger("CDMLoader")

class CdmProvider:
    def __init__(self, cdm_name: str, device_dir: Path, cdm_api_config: Optional[Dict[str, Any]] = None):
        self.cdm_name = cdm_name
        self.device_dir = device_dir
        self.cdm_api_config = cdm_api_config or {}
        self._cdm_instance: Optional[BaseCdm] = None

    @property
    def cdm_instance(self) -> BaseCdm:
        if self._cdm_instance is None:
            self._cdm_instance = self._load_cdm()
        return self._cdm_instance

    @property
    def is_playready(self) -> bool:
        return self.cdm_instance.cdm_type == "playready"
        
    @property
    def is_widevine(self) -> bool:
        return self.cdm_instance.cdm_type == "widevine"
        
    def _load_cdm(self) -> BaseCdm:
        local_path = self.device_dir / self.cdm_name
        if local_path.is_file():
            return self._load_local_cdm(local_path)

        for ext in ['.wvd', '.prd']:
            path_with_ext = self.device_dir / f"{self.cdm_name}{ext}"
            if path_with_ext.is_file():
                return self._load_local_cdm(path_with_ext)

        dev_dir = self.device_dir / self.cdm_name
        if dev_dir.is_dir():
            if (dev_dir / 'zgpriv.dat').is_file() and (dev_dir / 'bgroupcert.dat').is_file():
                prd_path = self._create_playready_device(dev_dir)
                if prd_path:
                    return self._load_local_cdm(prd_path)
            
            return self._load_local_dir(dev_dir)

        if self.cdm_name in self.cdm_api_config:
            return self._load_remote_cdm(self.cdm_api_config[self.cdm_name])

        raise ValueError(f"CDM '{self.cdm_name}' not found locally or in API config.")

    def _load_local_cdm(self, path: Path) -> BaseCdm:
        cdm_type = detect_cdm_type(path)
        
        if cdm_type == "widevine":
            try:
                from pywidevine.cdm import Cdm as PyWidevineCdm
                from pywidevine.device import Device as PyWidevineDevice
                device = PyWidevineDevice.load(path)
                return WidevineCdmAdapter(PyWidevineCdm.from_device(device))
            except ImportError:
                log.warning("pywidevine not installed, falling back to built-in legacy widevine.")
                from pywidevine.cdm import Cdm as LegacyWVCdm
                from pywidevine.device import LocalDevice as LegacyWVDevice
                device = LegacyWVDevice.load(path)
                return WidevineCdmAdapter(LegacyWVCdm(device))
            
        elif cdm_type == "playready":
            try:
                from pyplayready.cdm import Cdm as PyPlayReadyCdm
                from pyplayready.device import Device as PyPlayReadyDevice
                device = PyPlayReadyDevice.load(path)
                return PlayReadyCdmAdapter(PyPlayReadyCdm.from_device(device))
            except ImportError:
                log.warning("pyplayready not installed, falling back to built-in legacy playready.")
                from pyplayready.cdm import Cdm as LegacyPRCdm
                from pyplayready.device import Device as LegacyPRDevice
                device = LegacyPRDevice.load(path)
                return PlayReadyCdmAdapter(LegacyPRCdm.from_device(device))
        else:
            raise ValueError(f"Unsupported CDM file format: {path.suffix}")

    def _load_local_dir(self, path: Path) -> BaseCdm:
        if not path.is_dir():
            raise ValueError(f"CDM directory not found at: {path}")
            
        log.debug(f"Loading CDM from directory: {path}")
        from pywidevine.device import LocalDevice as LegacyWVDevice
        from pywidevine.cdm import Cdm as LegacyWVCdm
        device = LegacyWVDevice.from_dir(str(path))
        return WidevineCdmAdapter(LegacyWVCdm(device))

    def _create_playready_device(self, device_dir: Path) -> Optional[Path]:
        try:
            from pyplayready.crypto.ecc_key import ECCKey
            from pyplayready.system.bcert import CertificateChain, Certificate
            from pyplayready.device import Device as DevicePR
        except ImportError:
            log.error("Built-in pyplayready not available, cannot generate .prd from directory.")
            return None

        group_key_path = device_dir / 'zgpriv.dat'
        group_cert_path = device_dir / 'bgroupcert.dat'
        infofile = device_dir / 'PR.json'

        if infofile.is_file():
            try:
                with open(infofile, 'r') as f:
                    info = json.load(f)
                if "expiry" in info and datetime.fromisoformat(info["expiry"]) > datetime.now():
                    existing = device_dir / info["device"]
                    if existing.is_file():
                        log.info(f" + Loading existing generated PlayReady device: {info['device']}")
                        return existing
            except Exception:
                pass

        log.info(" + Generating new PlayReady Device (.prd) from directory...")
        try:
            enc_key = ECCKey.generate()
            sig_key = ECCKey.generate()

            gk_obj = ECCKey.load(group_key_path)
            chain = CertificateChain.load(group_cert_path)

            new_cert = Certificate.new_leaf_cert(
                cert_id=get_random_bytes(16),
                security_level=chain.get_security_level(),
                client_id=get_random_bytes(16),
                signing_key=sig_key,
                encryption_key=enc_key,
                group_key=gk_obj,
                parent=chain,
            )
            chain.prepend(new_cert)

            device = DevicePR(
                group_key=gk_obj.dumps(),
                encryption_key=enc_key.dumps(),
                signing_key=sig_key.dumps(),
                group_certificate=chain.dumps(),
            )

            expiry = (datetime.now() + timedelta(days=3650)).isoformat()
            raw = device.dumps()
            out_path = device_dir / f"{device.get_name()}_{raw[:4].hex()}.prd"

            if out_path.exists():
                log.error(f"Device file already exists: {out_path}")
                return None

            out_path.write_bytes(raw)

            with open(infofile, 'w') as f:
                json.dump({
                    "expiry": expiry,
                    "device": out_path.name,
                    "SecurityLevel": device.security_level,
                    "created": datetime.now().isoformat(),
                }, f)

            log.info(f" + Created PlayReady Device: {out_path.name}")
            return out_path

        except Exception as e:
            log.error(f"Failed to generate PlayReady device: {e}")
            return None

    def _load_remote_cdm(self, api_config: Dict[str, Any]) -> BaseCdm:
        from wpgskd.core.cdm.custom_remote_cdm import RemoteCdmAdapter
        log.info(f"Loading Remote CDM: {api_config.get('name')}")
        return RemoteCdmAdapter(api_config)

    def log_info(self):
        cdm = self.cdm_instance
        log.info(f" + CDM Type: {cdm.cdm_type.upper()}")
        log.info(f" + Security Level: L{cdm.security_level}")
        if cdm.system_id:
            log.info(f" + System ID: {cdm.system_id}")

class WidevineCdmAdapter(BaseCdm):
    def __init__(self, cdm_instance):
        self._cdm = cdm_instance

    @property
    def security_level(self): return self._cdm.security_level
    @property
    def system_id(self): return self._cdm.system_id
    @property
    def cdm_type(self): return "widevine"

    def open(self): return self._cdm.open()
    def close(self, session_id): self._cdm.close(session_id)
    
    def get_license_challenge(self, session_id, pssh_data, privacy_mode=True):
        try:
            from pywidevine.pssh import PSSH
            from wpgskd.vendor.pymp4.parser import Box as Pymp4Box
            if hasattr(pssh_data, 'type') and hasattr(pssh_data, 'init_data') and not isinstance(pssh_data, PSSH):
                pssh_bytes = Pymp4Box.build(pssh_data)
                pssh_data = PSSH(pssh_bytes)
        except Exception:
            pass
            
        if hasattr(self._cdm, 'get_license_challenge'):
            import inspect
            sig = inspect.signature(self._cdm.get_license_challenge)
            if 'service_name' in sig.parameters:
                return self._cdm.get_license_challenge(session_id, pssh_data, service_name="default")
            return self._cdm.get_license_challenge(session_id, pssh_data, privacy_mode=privacy_mode)

    def parse_license(self, session_id, license_message):
        self._cdm.parse_license(session_id, license_message)

    def get_keys(self, session_id, key_type="CONTENT"):
        keys = self._cdm.get_keys(session_id)
        result = []
        for k in keys:
            kid = k.kid.hex if hasattr(k.kid, 'hex') else str(k.kid).replace("-", "")
            key = k.key.hex() if isinstance(k.key, bytes) else str(k.key)
            result.append({"kid": kid, "key": key, "type": k.type})
        
        if key_type:
            return [k for k in result if k['type'] == key_type]
        return result

class PlayReadyCdmAdapter(BaseCdm):
    def __init__(self, cdm_instance):
        self._cdm = cdm_instance

    @property
    def security_level(self): return self._cdm.security_level
    @property
    def system_id(self): return 1 
    @property
    def cdm_type(self): return "playready"

    def open(self): return self._cdm.open()
    def close(self, session_id): self._cdm.close(session_id)
    
    def get_license_challenge(self, session_id, pssh_data, privacy_mode=True):
        return self._cdm.get_license_challenge(session_id, pssh_data)

    def parse_license(self, session_id, license_message):
        self._cdm.parse_license(session_id, license_message)

    def get_keys(self, session_id, key_type=None):
        keys = self._cdm.get_keys(session_id)
        result = []
        for k in keys:
            kid = k.key_id.hex if hasattr(k.key_id, 'hex') else str(k.key_id).replace("-", "")
            key = k.key.hex() if isinstance(k.key, bytes) else str(k.key)
            result.append({"kid": kid, "key": key, "type": "CONTENT"})
        return result
```

### `wpgskd\core\decryptors\__init__.py`

```python
from wpgskd.core.decryptors.aes import AES128Decryptor

__all__ = ['AES128Decryptor']
```

### `wpgskd\core\decryptors\aes.py`

```python
from Cryptodome.Cipher import AES
from wpgskd.core.decryptors.base import Decryptor

class AES128Decryptor(Decryptor):
    
    def __init__(self, key: bytes, iv: bytes = None):
        self.key = key
        self.iv = iv

    def decrypt(self, data: bytes, sequence_number: int = 0, **kwargs) -> bytes:
        current_iv = self.iv
        if not current_iv:
            current_iv = sequence_number.to_bytes(16, 'big')
            
        cipher = AES.new(self.key, AES.MODE_CBC, current_iv)
        
        try:
            return cipher.decrypt(data)
        except ValueError:
            return data
```

### `wpgskd\core\decryptors\base.py`

```python
from abc import ABC, abstractmethod

class Decryptor(ABC):
    @abstractmethod
    def decrypt(self, data: bytes, **kwargs) -> bytes:
        pass
```

### `wpgskd\core\drm\__init__.py`

```python
from wpgskd.core.drm.base import BaseDRM
from wpgskd.core.drm.widevine import Widevine
from wpgskd.core.drm.playready import PlayReady
from wpgskd.core.drm.clearkey import ClearKey

__all__ = ['BaseDRM', 'Widevine', 'PlayReady', 'ClearKey']
```

### `wpgskd\core\drm\base.py`

```python
from abc import ABC, abstractmethod
from typing import Any, Dict, Optional, Tuple

class BaseDRM(ABC):
    
    def __init__(self, cdm_provider: Any, service: Any):
        self.cdm_provider = cdm_provider
        self.service = service

    @abstractmethod
    def get_keys(self, track: Any, title: Any, session: Any) -> Tuple[Optional[str], Dict[str, str]]:
        pass
```

### `wpgskd\core\drm\clearkey.py`

```python
import logging
import base64
import requests
from typing import Any, Dict, Tuple, Optional
from wpgskd.core.drm.base import BaseDRM
from wpgskd.core.resolver import KeyResolver

log = logging.getLogger("DRM.ClearKey")

class ClearKey(BaseDRM):
    
    def get_keys(self, track: Any, title: Any, session: Any) -> Tuple[Optional[str], Dict[str, str]]:
        if getattr(track, 'key', None):
            kid = KeyResolver._norm(track.kid)
            return track.key, {kid: track.key}
            
        license_url = getattr(track, 'license_url', None)
        if not license_url:
            raise ValueError("Track missing license_url for ClearKey")
            
        kid_hex = track.kid.replace("-", "")
        kid_b64 = base64.b64encode(bytes.fromhex(kid_hex)).decode()
        
        payload = {"kids": [kid_b64], "type": "temporary"}
        
        try:
            res = session.post(license_url, json=payload)
            res.raise_for_status()
            data = res.json()
            
            k_b64 = data.get("keys", [{}])[0].get("k")
            if not k_b64:
                raise ValueError("No key returned from ClearKey server")
                
            key_hex = base64.b64decode(k_b64).hex()
            return key_hex, {kid_hex: key_hex}
            
        except Exception as e:
            raise ValueError(f"ClearKey request failed: {e}")
```

### `wpgskd\core\drm\drmtoday.py`

```python
# Most of these were taken from the old player JS.
# 40002 was inferred based on tests with actual keys.
DRMTODAY_RESPONSE_CODES = {
    "00000": "Success",
    "01000": "General Internal Error",
    "02000": "General Request Error",
    "03000": "General Request Authentication Error",
    "30000": "General DRM Error",
    "40000": "General Widevine Modular Error",
    "40001": "Widevine Device Certificate Revocation",
    "40002": "Widevine Device Certificate Serial Number Revocation",
    "41000": "General Widevine Classic Error",
    "42000": "General PlayReady Error",
    "43000": "General FairPlay Error",
    "44000": "General OMA Error",
    "44001": "OMA Device Registration Failed",
    "45000": "General CDRM Error",
    "45001": "CDRM Device Registration Failed",
    "70000": "General Output Protection Error",
    "70001": "All keys filtered by EOP settings",
    "80000": "General CSL Error",
    "80001": "Too many concurrent streams",
    "90000": "General GBL Error",
    "90001": "License delivery prohibited in your region"
}
```

### `wpgskd\core\drm\playready.py`

```python
import logging
import base64
from typing import Any, Dict, Tuple, Optional
from wpgskd.core.drm.base import BaseDRM
from wpgskd.core.resolver import KeyResolver

log = logging.getLogger("DRM.PlayReady")

class PlayReady(BaseDRM):
    
    def get_keys(self, track: Any, title: Any, session: Any) -> Tuple[Optional[str], Dict[str, str]]:
        cdm = self.cdm_provider.cdm_instance
        
        if cdm.cdm_type != "playready":
            raise ValueError("CDM is not a PlayReady CDM")
            
        pr_pssh = getattr(track, 'pr_pssh', None)
        if not pr_pssh:
            raise ValueError("Track missing PR_PSSH for PlayReady CDM")
            
        try:
            from pyplayready.system.pssh import PSSH as PRPSSH
            wrm = PRPSSH(pr_pssh).wrm_headers[0]
        except Exception:
            raise ValueError("Failed to parse WRM Header from PR_PSSH")

        sid = cdm.open()
        try:
            challenge = cdm.get_license_challenge(sid, wrm).encode('utf-8')
            license_res = self.service.license(
                challenge=challenge, title=title, track=track, session_id=sid
            )
            
            if isinstance(license_res, bytes):
                if b"<License>" in license_res:
                    license_res = base64.b64encode(license_res).decode()
                else:
                    license_res = base64.b64decode(license_res).decode()
                    
            cdm.parse_license(sid, license_res)
            
            keys_list = cdm.get_keys(sid)
            result = {}
            target_kid = KeyResolver._norm(track.kid)
            
            for k in keys_list:
                kid = KeyResolver._norm(k.get('kid'))
                key = k.get('key')
                if kid and key and kid != "00" * 16:
                    result[kid] = key.lower()

            primary_key = result.get(target_kid)
            if not primary_key and result:
                primary_key = next(iter(result.values()))
                log.warning(f"No exact KID match for {track.kid}, using fallback key.")
                
            return primary_key, result
            
        except Exception as e:
            raise ValueError(f"PlayReady license request failed: {e}")
        finally:
            cdm.close(sid)
```

### `wpgskd\core\drm\widevine.py`

```python
import logging
from typing import Any, Dict, Tuple, Optional
from wpgskd.core.drm.base import BaseDRM
from wpgskd.core.resolver import KeyResolver

log = logging.getLogger("DRM.Widevine")

class Widevine(BaseDRM):
    
    def get_keys(self, track: Any, title: Any, session: Any) -> Tuple[Optional[str], Dict[str, str]]:
        cdm = self.cdm_provider.cdm_instance
        
        if cdm.cdm_type != "widevine":
            raise ValueError("CDM is not a Widevine CDM")
            
        pssh_data = getattr(track, 'pssh', None)
        if not pssh_data:
            raise ValueError("Track missing PSSH for Widevine CDM")
            
        sid = cdm.open()
        try:
            challenge = cdm.get_license_challenge(sid, pssh_data, privacy_mode=True)
            license_res = self.service.license(
                challenge=challenge, title=title, track=track, session_id=sid
            )
            cdm.parse_license(sid, license_res)
            
            keys_list = cdm.get_keys(sid)
            result = {}
            target_kid = KeyResolver._norm(track.kid)
            
            for k in keys_list:
                kid = KeyResolver._norm(k.get('kid'))
                key = k.get('key')
                if kid and key and kid != "00" * 16:
                    result[kid] = key.lower()

            primary_key = result.get(target_kid)
            if not primary_key and result:
                primary_key = next(iter(result.values()))
                log.warning(f"No exact KID match for {track.kid}, using fallback key.")
                
            return primary_key, result
            
        except Exception as e:
            raise ValueError(f"Widevine license request failed: {e}")
        finally:
            cdm.close(sid)
```

### `wpgskd\core\manifests\__init__.py`

```python
from wpgskd.core.manifests.dash import parse as parse_mpd
from wpgskd.core.manifests.hls import parse as parse_hls
from wpgskd.core.manifests.ism import parse as parse_ism
from wpgskd.core.manifests.map_init import extract_pssh_and_kid
from wpgskd.core.manifests.m3u8 import parse_media_playlist, fetch_pssh_and_kid_from_m3u8, fetch_aes_keys_from_m3u8

from wpgskd.core.manifests import hls as m3u8
from wpgskd.core.manifests import dash as mpd
from wpgskd.core.manifests import ism

__all__ = [
    "parse_mpd", "parse_hls", "parse_ism", 
    "extract_pssh_and_kid", 
    "parse_media_playlist", "fetch_pssh_and_kid_from_m3u8", "fetch_aes_keys_from_m3u8",
    "m3u8", "mpd", "ism"
]
```

### `wpgskd\core\manifests\dash.py`

```python
import xmltodict
import asyncio
import base64
import json
import logging
import math
import os
import re 
import urllib.parse
import uuid
from copy import copy
from hashlib import md5
from typing import Optional

import requests
from langcodes import Language
from langcodes.tag_parser import LanguageTagError

from wpgskd.config import config, directories
from wpgskd.core.tracks import AudioTrack, TextTrack, Track, Tracks, VideoTrack
from wpgskd.core.utilities import Cdm
from wpgskd.core.io import aria2c
from wpgskd.core.xml import load_xml
from wpgskd.vendor.pymp4.parser import Box

log = logging.getLogger("MPD")

def parse(*, url=None, data=None, source, session=None, downloader=None, multi_period=False):
    if not data:
        if not url:
            raise ValueError("Neither a URL nor a document was provided to Tracks.from_mpd")

        if downloader is None:
            data = (session or requests).get(url).text
        elif downloader == "aria2c":
            out = os.path.join(directories.temp, url.split("/")[-1])
            asyncio.run(aria2c(url, out))
            with open(out, encoding="utf-8") as fd:
                data = fd.read()
            try:
                os.unlink(out)
            except FileNotFoundError:
                pass
        else:
            raise ValueError(f"Unsupported downloader: {downloader}")

    root = load_xml(data)
    if root.tag != "MPD":
        raise ValueError("Non-MPD document provided to Tracks.from_mpd")

    if multi_period:
        log.info(f" + Using multi-period parser for {source}")
    else:
        log.debug(f" + Using single-period parser for {source}")

    return _parse_mpd(root, url, source, session)

def _parse_mpd(root, url, source, session):
    import re
    import xml.etree.ElementTree as ET

    namespace_match = re.match(r'\{([^}]+)\}', root.tag)
    namespace_uri = namespace_match.group(1) if namespace_match else "urn:mpeg:dash:schema:mpd:2011"

    if namespace_match:
        periods = root.findall(f".//{{{namespace_uri}}}Period")
    else:
        periods = root.findall(".//Period")

    is_multi_period = len(periods) > 1
    period_tracks_list = []

    root_base_url = root.findtext("BaseURL")
    periods_to_process = periods if is_multi_period else [root]

    for period_idx, period_elem in enumerate(periods_to_process):
        if is_multi_period:
            log.debug(f" + Processing period {period_idx + 1}/{len(periods)}")

            period_str = ET.tostring(period_elem, encoding='unicode', method='xml')
            virtual_mpd = f'''<?xml version="1.0" encoding="UTF-8"?>
<MPD xmlns="{namespace_uri}"
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
     xmlns:cenc="urn:mpeg:cenc:2013"
     xmlns:mspr="urn:microsoft:playready"
     profiles="urn:mpeg:dash:profile:isoff-live:2011"
     type="static"
     minBufferTime="PT2S"
     mediaPresentationDuration="{root.get('mediaPresentationDuration', 'PT0S')}">
  {period_str}
</MPD>'''

            virtual_mpd = virtual_mpd.replace('ns0:default_KID', 'cenc:default_KID')
            virtual_mpd = virtual_mpd.replace('ns0:pssh', 'cenc:pssh')
            virtual_mpd = virtual_mpd.replace('ns0:pro', 'mspr:pro')
            virtual_mpd = virtual_mpd.replace('xmlns:ns0', 'xmlns:cenc')
            virtual_mpd = re.sub(r'<!--.*?-->', '', virtual_mpd, flags=re.DOTALL)

            try:
                period_root = load_xml(virtual_mpd)
            except Exception as e:
                log.warning(f" + Failed to parse period {period_idx + 1}: {e}")
                new_root = ET.Element('MPD', attrib={
                    'xmlns': namespace_uri,
                    'xmlns:xsi': 'http://www.w3.org/2001/XMLSchema-instance',
                    'xmlns:cenc': 'urn:mpeg:cenc:2013',
                    'xmlns:mspr': 'urn:microsoft:playready',
                    'profiles': 'urn:mpeg:dash:profile:isoff-live:2011',
                    'type': 'static',
                    'minBufferTime': 'PT2S',
                    'mediaPresentationDuration': root.get('mediaPresentationDuration', 'PT0S')
                })
                new_root.append(period_elem)
                temp_mpd = ET.tostring(new_root, encoding='unicode', method='xml')
                temp_mpd = temp_mpd.replace('ns0:default_KID', 'cenc:default_KID')
                temp_mpd = temp_mpd.replace('ns0:pssh', 'cenc:pssh')
                temp_mpd = temp_mpd.replace('ns0:pro', 'mspr:pro')
                temp_mpd = temp_mpd.replace('xmlns:ns0', 'xmlns:cenc')
                period_root = load_xml(temp_mpd)
        else:
            period_root = root
            period_elem = root

        tracks = []

        found_period = period_root.find(".//Period")
        search_periods = (period_root.findall("Period")
                          if not is_multi_period
                          else [found_period if found_period is not None else period_root])

        for period in search_periods:
            if period is None:
                period = period_root if period_root.tag == "Period" else period_root

            if source == "HULU" and next(iter(period.xpath("SegmentType/@value")), "content") != "content":
                continue

            period_base_url = period.findtext("BaseURL") or root_base_url
            if url and period_base_url and not re.match("^https?://", period_base_url.lower()):
                period_base_url = period_base_url.replace('fly.eu.prd.media.max.com', 'akm.eu.prd.media.max.com')
                period_base_url = period_base_url.replace('gcp.eu.prd.media.max.com', 'akm.eu.prd.media.max.com')
                period_base_url = period_base_url.replace('fly.latam.prd.media.max.com', 'akm.latam.prd.media.max.com')
                period_base_url = period_base_url.replace('gcp.latam.prd.media.max.com', 'akm.latam.prd.media.max.com')
            period_duration = period.get("duration")
            if period_duration:
                period_duration = Track.pt_to_sec(period_duration)
            mpd_duration = root.get("mediaPresentationDuration")
            if mpd_duration:
                mpd_duration = Track.pt_to_sec(mpd_duration)

            for adaptation_set in period.findall("AdaptationSet"):
                if any(x.get("schemeIdUri") == "http://dashif.org/guidelines/trickmode"
                       for x in adaptation_set.findall("EssentialProperty")
                       + adaptation_set.findall("SupplementalProperty")):
                    continue

                for rep in adaptation_set.findall("Representation"):
                    try:
                        content_type = next(x for x in [
                            rep.get("contentType"),
                            rep.get("mimeType"),
                            adaptation_set.get("contentType"),
                            adaptation_set.get("mimeType")
                        ] if bool(x))
                    except StopIteration:
                        raise ValueError("No content type value could be found")
                    else:
                        content_type = content_type.split("/")[0]
                    if content_type.startswith("image"):
                        continue

                    codecs = rep.get("codecs") or adaptation_set.get("codecs")
                    supplementalcodecs = (rep.get("{urn:scte:dash:scte214-extensions}supplementalCodecs")
                                          or adaptation_set.get("{urn:scte:dash:scte214-extensions}supplementalCodecs"))
                    if content_type in ("text", "application"):
                        mime = adaptation_set.get("mimeType")
                        if mime and not mime.endswith("/mp4"):
                            codecs = mime.split("/")[1]

                    track_lang = None
                    for lang in [rep.get("lang"), adaptation_set.get("lang")]:
                        lang = (lang or "").strip()
                        if not lang:
                            continue
                        try:
                            t = Language.get(lang.split("-")[0])
                            if t == Language.get("und") or not t.is_valid():
                                raise LanguageTagError()
                        except LanguageTagError:
                            continue
                        else:
                            track_lang = Language.get(lang)
                            break

                    protections = rep.findall("ContentProtection") + adaptation_set.findall("ContentProtection")
                    encrypted = bool(protections)
                    pssh = None
                    pr_pssh = None

                    kid = None

                    for protection in adaptation_set.findall("ContentProtection"):
                        if protection.get("schemeIdUri") == "urn:mpeg:dash:mp4protection:2011":
                            kid_val = protection.get("{urn:mpeg:cenc:2013}default_KID")
                            if kid_val:
                                kid = uuid.UUID(kid_val).hex.lower()
                                log.debug(f" + KID from AdaptationSet {adaptation_set.get('id', '?')} "
                                          f"for {content_type}: {kid}")
                                break

                    if not kid:
                        for protection in rep.findall("ContentProtection"):
                            if protection.get("schemeIdUri") == "urn:mpeg:dash:mp4protection:2011":
                                kid_val = protection.get("{urn:mpeg:cenc:2013}default_KID")
                                if kid_val:
                                    kid = uuid.UUID(kid_val).hex.lower()
                                    log.debug(f" + KID from Representation for {content_type}: {kid}")
                                    break

                    if not kid and content_type == "audio":
                        for protection in period.findall(".//ContentProtection"):
                            if protection.get("schemeIdUri") == "urn:mpeg:dash:mp4protection:2011":
                                kid_val = protection.get("{urn:mpeg:cenc:2013}default_KID")
                                if kid_val:
                                    kid = uuid.UUID(kid_val).hex.lower()
                                    log.debug(f" + Audio inheriting KID from video: {kid}")
                                    break

                    for protection in protections:
                        if "9a04f079-9840-4286-ab92-e65be0885f95" in protection.get("schemeIdUri", "").lower():
                            pr_pssh = protection.findtext("pro") or protection.findtext("pssh")
                        if (protection.get("schemeIdUri") or "").lower() != Cdm.urn:
                            continue
                        pssh = protection.findtext("pssh")
                        if pssh:
                            pssh_bytes = base64.b64decode(pssh)
                            try:
                                from pywidevine.pssh import PSSH
                                pssh = PSSH(pssh_bytes)
                            except Exception:
                                try:
                                    pssh = Box.parse(pssh_bytes)
                                except Exception:
                                    pssh = Box.parse(Box.build(dict(
                                        type=b"pssh",
                                        version=0,
                                        flags=0,
                                        system_ID=Cdm.uuid,
                                        init_data=pssh_bytes
                                    )))

                    track_url = url

                    seg_list_rep = rep.find("SegmentList")
                    seg_list_as = adaptation_set.find("SegmentList")
                    segment_list = seg_list_rep if seg_list_rep is not None else seg_list_as

                    seg_tpl_rep = rep.find("SegmentTemplate")
                    seg_tpl_as = adaptation_set.find("SegmentTemplate")
                    segment_template = seg_tpl_rep if seg_tpl_rep is not None else seg_tpl_as
                    
                    if segment_list is None and segment_template is None:
                        rep_base_url = rep.findtext("BaseURL")
                        if rep_base_url:
                            if not re.match("^https?://", rep_base_url.lower()):
                                rep_base_url = urllib.parse.urljoin(period_base_url, rep_base_url)
                            query = urllib.parse.urlparse(url).query
                            if query and not urllib.parse.urlparse(rep_base_url).query:
                                rep_base_url += "?" + query
                            track_url = rep_base_url

                    track_id = "{codec}-{lang}-{bitrate}-{extra}".format(
                        codec=codecs,
                        lang=track_lang,
                        bitrate=rep.get("bandwidth") or 0,
                        extra=(adaptation_set.get("audioTrackId") or "") + (rep.get("id") or ""),
                    )
                    track_id = md5(track_id.encode()).hexdigest()

                    def get_track_size(track_repr):
                        segment_list = track_repr.findall('SegmentList')
                        if segment_list:
                            file_size = sorted(
                                segment_list[0].findall('SegmentURL'),
                                key=lambda seg_url: int(seg_url.get('mediaRange').split('-')[1]),
                                reverse=True
                            )
                            if file_size:
                                return int(file_size[0].get('mediaRange').split('-')[1])
                        return None

                    if content_type == "video":
                        fps_str = rep.get("frameRate") or adaptation_set.get("frameRate")
                        fps = None
                        if fps_str:
                            try:
                                if "/" in fps_str:
                                    num, den = fps_str.split("/")
                                    fps = float(num) / float(den)
                                else:
                                    fps = float(fps_str)
                            except ValueError:
                                fps = None
                        
                        if not fps:
                            fps = _calculate_fps_from_timeline(rep, period)
                            if fps:
                                log.debug(f" + Calculated FPS {fps} for video track "
                                          f"(codec: {codecs}, resolution: "
                                          f"{rep.get('width')}x{rep.get('height')})")
                        
                        vt = VideoTrack(
                            id_=track_id,
                            source=source,
                            url=track_url,
                            codec=(codecs or "").split(".")[0],
                            language=track_lang,
                            bitrate=rep.get("bandwidth"),
                            width=int(rep.get("width") or 0) or adaptation_set.get("width"),
                            height=int(rep.get("height") or 0) or adaptation_set.get("height"),
                            fps=fps,
                            hdr10=any(
                                x.get("schemeIdUri") == "urn:mpeg:mpegB:cicp:TransferCharacteristics"
                                and x.get("value") == "16"
                                for x in adaptation_set.findall("SupplementalProperty") + adaptation_set.findall("EssentialProperty")
                            ) or any(
                                x.get("schemeIdUri") == "http://dashif.org/metadata/hdr"
                                and x.get("value") == "SMPTE2094-40"
                                for x in adaptation_set.findall("SupplementalProperty") + adaptation_set.findall("EssentialProperty")
                            ),
                            hlg=any(
                                x.get("schemeIdUri") == "urn:mpeg:mpegB:cicp:TransferCharacteristics"
                                and x.get("value") == "18"
                                for x in adaptation_set.findall("SupplementalProperty")
                            ),
                            dvhdr=(
                                (isinstance(codecs, str) and codecs.startswith(("dvhe.08", "dvh1.08")))
                                or (isinstance(supplementalcodecs, str) and "dvh1.08" in supplementalcodecs)
                            ),
                            dv=codecs and codecs.startswith(("dvhe", "dvh1")),
                            descriptor=Track.Descriptor.MPD,
                            encrypted=encrypted,
                            pssh=pssh,
                            pr_pssh=pr_pssh,
                            kid=kid,
                            duration=mpd_duration or period_duration,
                            extra=(rep, adaptation_set)
                        )
                        vt.manifest_url = url
                        vt.mpd_representation_id = rep.get("id")
                        tracks.append(vt)

                    elif content_type == "audio":
                        at = AudioTrack(
                            id_=track_id,
                            source=source,
                            url=track_url,
                            codec=(codecs or "").split(".")[0],
                            language=track_lang,
                            bitrate=rep.get("bandwidth"),
                            channels=next(iter(
                                rep.xpath("AudioChannelConfiguration/@value")
                                or adaptation_set.xpath("AudioChannelConfiguration/@value")
                            ), None),
                            descriptive=any(
                                (x.get("schemeIdUri") == "urn:mpeg:dash:role:2011"
                                 and x.get("value") == "description")
                                or (x.get("schemeIdUri") == "urn:tva:metadata:cs:AudioPurposeCS:2007"
                                    and x.get("value") == "1")
                                for x in adaptation_set.findall("Accessibility")
                            ),
                            atmos=any(
                                prop.get("schemeIdUri") == "tag:dolby.com,2018:dash:EC3_ExtensionType:2018"
                                and prop.get("value") == "JOC"
                                for prop in rep.findall("SupplementalProperty")
                            ),
                            descriptor=Track.Descriptor.MPD,
                            encrypted=encrypted,
                            pssh=pssh,
                            pr_pssh=pr_pssh,
                            kid=kid,
                            duration=mpd_duration or period_duration,
                            extra=(rep, adaptation_set)
                        )
                        at.manifest_url = url
                        at.mpd_representation_id = rep.get("id")
                        tracks.append(at)

                    elif content_type in ("text", "application"):
                        role_elem = adaptation_set.find(".//{*}Role")
                        role = role_elem.get("value") if role_elem is not None else ""

                        is_forced = (role == "forced-subtitle")
                        is_sdh = (role == "caption") or (role == "sdh")
                        is_normal = (role == "subtitle") or (role == "main") or (not role)

                        adapt_set_id = adaptation_set.get("id", "")
                        if not is_forced and ("forced" in adapt_set_id.lower()
                                              or "fn" in adapt_set_id.lower()):
                            is_forced = True
                            log.debug(f" + Detected forced subtitle by adaptation set ID: {adapt_set_id}")

                        rep_id = rep.get("id", "")
                        if not is_forced and ("forced" in rep_id.lower()
                                              or "fn" in rep_id.lower()):
                            is_forced = True
                            log.debug(f" + Detected forced subtitle by representation ID: {rep_id}")

                        if not is_forced and codecs and ("forced" in codecs.lower()
                                                         or "fn" in codecs.lower()):
                            is_forced = True
                            log.debug(f" + Detected forced subtitle by codec pattern: {codecs}")

                        if source == 'HMAX':
                            seg_tpl = rep.find("SegmentTemplate")
                            sub_path_url = rep.findtext("BaseURL")
                            if not sub_path_url:
                                sub_path_url = seg_tpl.get('media') if seg_tpl else None

                            if not sub_path_url:
                                continue

                            try:
                                path = re.search(r'(t\/.+?\/)t', sub_path_url).group(1)
                            except AttributeError:
                                path = 't/sub/'

                            if is_normal:
                                track_url = period_base_url + path + adaptation_set.get('lang') + '_sub.vtt'
                            elif is_sdh:
                                track_url = period_base_url + path + adaptation_set.get('lang') + '_sdh.vtt'
                            elif is_forced:
                                track_url = period_base_url + path + adaptation_set.get('lang') + '_forced.vtt'
                            else:
                                track_url = period_base_url + path + adaptation_set.get('lang') + '_sub.vtt'

                            if seg_tpl is not None and seg_tpl.get('media') and '$Number$' in seg_tpl.get('media'):
                                media_pattern = seg_tpl.get('media')
                                if not re.match("^https?://", media_pattern):
                                    media_pattern = urllib.parse.urljoin(period_base_url, media_pattern)
                                track_url = media_pattern

                            tt = TextTrack(
                                id_=track_id,
                                source=source,
                                url=track_url,
                                codec=(codecs or "").split(".")[0] if codecs else "vtt",
                                language=track_lang,
                                forced=is_forced,
                                sdh=is_sdh,
                                descriptor=Track.Descriptor.MPD,
                                extra=(rep, adaptation_set)
                            )
                            tt.manifest_url = url
                            tt.mpd_representation_id = rep.get("id")
                            tracks.append(tt)
                        else:
                            extra_info = {
                                "role": role,
                                "adaptation_set_id": adapt_set_id,
                                "representation_id": rep_id,
                                "original_forced_detection": is_forced
                            }

                            if track_url and isinstance(track_url, list):
                                for url_check in track_url:
                                    if isinstance(url_check, str) and (
                                        "forced" in url_check.lower()
                                        or "_fn" in url_check.lower()
                                        or "forced-subtitle" in url_check.lower()
                                    ):
                                        is_forced = True
                                        extra_info["detected_by_url"] = True
                                        log.debug(f" + Detected forced subtitle by URL pattern: {url_check}")
                                        break

                            tt = TextTrack(
                                id_=track_id,
                                source=source,
                                url=track_url,
                                codec=(codecs or "").split(".")[0] if codecs else "vtt",
                                language=track_lang,
                                forced=is_forced,
                                sdh=is_sdh,
                                descriptor=Track.Descriptor.MPD,
                                encrypted=encrypted,
                                pssh=pssh,
                                pr_pssh=pr_pssh,
                                kid=kid,
                                extra=extra_info
                            )
                            tt.manifest_url = url
                            tt.mpd_representation_id = rep.get("id")
                            tracks.append(tt)

        period_tracks_obj = Tracks()
        period_tracks_obj.add(tracks, warn_only=True)

        if is_multi_period:
            for track in (period_tracks_obj.videos
                         + period_tracks_obj.audios
                         + period_tracks_obj.subtitles):
                if not isinstance(track.url, list):
                    track.url = [track.url]
            period_tracks_list.append(period_tracks_obj)
        else:
            return period_tracks_obj

    if is_multi_period:
        return _merge_periods(period_tracks_list, source, log)

    return Tracks()

def _calculate_fps_from_timeline(rep, period, timescale_multiplier=1):
    import statistics
    segment_template = rep.find("SegmentTemplate")
    if segment_template is None:
        parent = rep.getparent()
        if parent is not None:
            segment_template = parent.find("SegmentTemplate")

    if segment_template is None:
        return None

    timescale = int(segment_template.get("timescale", 24000))
    timescale = timescale * timescale_multiplier

    segment_timeline = segment_template.find("SegmentTimeline")
    if segment_timeline is None:
        return None

    durations = []
    for s in segment_timeline.findall("S"):
        d = int(s.get("d", 0))
        if d > 0:
            repeat = int(s.get("r", 0))
            if repeat > 0:
                durations.extend([d] * (repeat + 1))
            else:
                durations.append(d)

    if not durations:
        return None

    if len(durations) > 1:
        try:
            variance = statistics.variance(durations) if len(durations) > 1 else 0
            if variance > 100:
                log.debug(f" + Detected VFR content (variance={variance:.2f})")
                avg_duration_ticks = statistics.median(durations)
            else:
                avg_duration_ticks = sum(durations) / len(durations)
        except (statistics.StatisticsError, TypeError):
            avg_duration_ticks = sum(durations) / len(durations)
    else:
        avg_duration_ticks = durations[0]

    avg_duration_sec = avg_duration_ticks / timescale

    if avg_duration_sec <= 0:
        return None

    fps = 1.0 / avg_duration_sec

    for common_fps in [23.976, 24.0, 25.0, 29.97, 30.0, 50.0, 59.94, 60.0]:
        if abs(fps - common_fps) < 0.01:
            fps = common_fps
            break

    log.debug(f" + Calculated FPS {fps:.3f} from {len(durations)} segments "
              f"(timescale={timescale}, avg_duration_ticks={avg_duration_ticks:.2f})")
    return round(fps, 3)

def _merge_periods(period_tracks_list, source, log):
    if not period_tracks_list:
        return Tracks()

    if len(period_tracks_list) == 1:
        return period_tracks_list[0]

    combined = Tracks()

    seen_videos = {}
    seen_audios = {}
    seen_subs = {}

    for period_tracks in period_tracks_list:
        for video in period_tracks.videos:
            key = getattr(video, 'mpd_representation_id', None) or (video.width, video.height, video.codec, video.bitrate, video.hdr10, video.dv)
            if key not in seen_videos:
                new_video = video
                new_video.url = []
                seen_videos[key] = new_video

            if isinstance(video.url, list):
                seen_videos[key].url.extend(video.url)
            else:
                seen_videos[key].url.append(video.url)

        for audio in period_tracks.audios:
            lang = str(audio.language) if audio.language else "und"
            if lang not in seen_audios:
                new_audio = audio
                new_audio.url = []
                seen_audios[lang] = new_audio

            if isinstance(audio.url, list):
                seen_audios[lang].url.extend(audio.url)
            else:
                seen_audios[lang].url.append(audio.url)

        for sub in period_tracks.subtitles:
            lang = str(sub.language) if sub.language else "und"
            sub_type = "forced" if sub.forced else "sdh" if sub.sdh else "normal"
            key = f"{lang}_{sub_type}"

            if key not in seen_subs:
                seen_subs[key] = sub
                if not isinstance(seen_subs[key].url, list):
                    seen_subs[key].url = [seen_subs[key].url]

    combined.videos = list(seen_videos.values())
    combined.audios = list(seen_audios.values())
    combined.subtitles = list(seen_subs.values())

    log.debug(f" + Merged {len(period_tracks_list)} periods into: "
              f"{len(combined.videos)} video, {len(combined.audios)} audio, "
              f"{len(combined.subtitles)} subtitle tracks")

    return combined
```

### `wpgskd\core\manifests\hls.py`

```python
import base64
import re
import logging
from hashlib import md5
import m3u8

from wpgskd.core.tracks import AudioTrack, TextTrack, Track, Tracks, VideoTrack
from wpgskd.constants import EncryptionScheme
from wpgskd.core.utilities import Cdm
from wpgskd.vendor.pymp4.parser import Box

log = logging.getLogger("HLSParser")

def parse(master, source=None, session=None):
    """
    Convert a Variant Playlist M3U8 document to a Tracks object with Video, Audio and
    Subtitle Track objects. This is not an M3U8 parser, use https://github.com/globocom/m3u8
    to parse, and then feed the parsed M3U8 object.

    :param master: M3U8 object of the `m3u8` project: https://github.com/globocom/m3u8
    :param source: Source tag for the returned tracks.
    """
    if not master.is_variant:
        raise ValueError("Tracks.from_m3u8: Expected a Variant Playlist M3U8 document...")

    # Get PSSH if available
    # Uses master.session_keys instead of master.keys as master.keys is ONLY EXT-X-KEYS and
    # doesn't include EXT-X-SESSION-KEYS which is what's used for variant playlist M3U8.
    widevine_urn = "urn:uuid:edef8ba9-79d6-4ace-a3c8-27dcd51d21ed"
    widevine_keys = [x.uri for x in master.session_keys
                     if x.keyformat and x.keyformat.lower() == widevine_urn]
    pssh = widevine_keys[0].split(",")[-1] if widevine_keys else None

    pr_keys = [x.uri for x in master.session_keys
               if x.keyformat and "playready" in x.keyformat.lower()]
    pr_pssh = pr_keys[0].split(",")[-1] if pr_keys else None

    if pssh:
        pssh = base64.b64decode(pssh)
        try:
            pssh = Box.parse(pssh)
        except Exception:
            pssh = Box.parse(Box.build(dict(
                type=b"pssh",
                version=0,
                flags=0,
                system_ID=Cdm.uuid,
                init_data=pssh
            )))

    # Also check top-level keys (non-session) as fallback
    if not pssh and not pr_pssh:
        widevine_top = [x.uri for x in master.keys
                        if x.keyformat and x.keyformat.lower() == widevine_urn]
        if widevine_top:
            pssh_raw = widevine_top[0].split(",")[-1]
            pssh_raw = base64.b64decode(pssh_raw)
            try:
                pssh = Box.parse(pssh_raw)
            except Exception:
                pssh = Box.parse(Box.build(dict(
                    type=b"pssh",
                    version=0,
                    flags=0,
                    system_ID=Cdm.uuid,
                    init_data=pssh_raw
                )))

        pr_top = [x.uri for x in master.keys
                  if x.keyformat and "playready" in x.keyformat.lower()]
        if pr_top:
            pr_pssh = pr_top[0].split(",")[-1]

    # Determine default encryption scheme
    default_scheme = EncryptionScheme.NONE
    if pssh:
        default_scheme = EncryptionScheme.WIDEVINE
    elif pr_pssh:
        default_scheme = EncryptionScheme.PLAYREADY

    # Check for AES-128 keys at master level
    aes128_keys = [x for x in (master.keys + master.session_keys)
                   if x.method and x.method.upper() == "AES-128"]
    if aes128_keys and not pssh and not pr_pssh:
        default_scheme = EncryptionScheme.AES_128

    has_encryption = bool(pssh or pr_pssh or aes128_keys or master.keys or master.session_keys)

    tracks_obj = Tracks()

    # ==================== VIDEO TRACKS ====================
    for x in master.playlists:
        stream_info = x.stream_info
        
        codec_str = _safe_get_codec(stream_info)
        resolution = _safe_get_resolution(stream_info)

        tracks_obj.add(VideoTrack(
            id_=md5(str(x).encode()).hexdigest()[0:7],
            source=source,
            url=("" if re.match("^https?://", x.uri) else x.base_uri) + x.uri,
            codec=codec_str,
            language=None,  # playlists don't state the language, fallback must be used
            bitrate=_safe_get_bitrate(stream_info),
            width=resolution[0],
            height=resolution[1],
            fps=_safe_get_frame_rate(stream_info),
            hdr10=(not _is_dv(codec_str) and _safe_get_video_range(stream_info) != "SDR"),
            hlg=False,
            dv=_is_dv(codec_str),
            descriptor=Track.Descriptor.M3U,
            encryption_scheme=default_scheme,
            encrypted=has_encryption,
            extra={"original": x, "master_pssh": pssh, "master_pr_pssh": pr_pssh} 
        ))

    # ==================== AUDIO + SUBTITLE TRACKS ====================
    if hasattr(master, 'media') and master.media:
        for x in master.media:
            # === AUDIO ===
            if x.type == "AUDIO" and x.uri:
                channels = x.channels if hasattr(x, 'channels') else None
                group_id = x.group_id if hasattr(x, 'group_id') else None
                bitrate = 0
                
                if group_id:
                    br_match = re.search(r'_(\d+)$', group_id)
                    if br_match:
                        bitrate = int(br_match.group(1)) * 1000
                    
                    if not channels:
                        ch_match = re.search(r'(\d+)ch', group_id)
                        if ch_match:
                            channels = f"{ch_match.group(1)}.0"

                characteristics = x.characteristics or "" if hasattr(x, 'characteristics') else ""

                tracks_obj.add(AudioTrack(
                    id_=md5(str(x).encode()).hexdigest()[0:6],
                    source=source,
                    url=("" if re.match("^https?://", x.uri) else x.base_uri) + x.uri,
                    codec=_safe_get_audio_codec(x),
                    language=x.language,
                    bitrate=bitrate,
                    channels=channels,
                    atmos=(channels or "").endswith("/JOC"),
                    descriptive="public.accessibility.describes-video" in characteristics,
                    descriptor=Track.Descriptor.M3U,
                    encryption_scheme=default_scheme,
                    encrypted=has_encryption,
                    extra={"original": x, "master_pssh": pssh, "master_pr_pssh": pr_pssh} 
                ))

            # === SUBTITLES ===
            elif x.type == "SUBTITLES" and x.uri:
                forced = x.forced == "YES" if hasattr(x, 'forced') else False
                characteristics = x.characteristics or "" if hasattr(x, 'characteristics') else ""
                name = x.name if hasattr(x, 'name') else ""
                group_id = x.group_id if hasattr(x, 'group_id') else ""
                
                is_cc = "cc" in name.lower() or "cc" in group_id.lower()

                tracks_obj.add(TextTrack(
                    id_=md5(str(x).encode()).hexdigest()[0:6],
                    source=source,
                    url=("" if re.match("^https?://", x.uri) else x.base_uri) + x.uri,
                    codec="vtt",
                    language=x.language,
                    forced=forced,
                    sdh="public.accessibility.describes-music-and-sound" in characteristics or is_cc,
                    descriptor=Track.Descriptor.M3U,
                    encryption_scheme=default_scheme,
                    encrypted=has_encryption,
                    extra={"original": x, "master_pssh": pssh, "master_pr_pssh": pr_pssh} 
                ))

    if tracks_obj.videos:
        try:
            from wpgskd.core.session import SessionBuilder
            s = session or SessionBuilder.build()
        except ImportError:
            import requests as req_mod
            s = session or req_mod.Session()
            
        first_video = tracks_obj.videos[0]
        try:
            sub_url = first_video.url
            if isinstance(sub_url, list):
                sub_url = sub_url[0]
            res = s.get(sub_url, timeout=10)
            res.raise_for_status()
            sub_m3u8 = m3u8.loads(res.text, uri=sub_url)
            
            total_duration = sum(seg.duration for seg in sub_m3u8.segments if seg.duration)
            fps = _infer_fps_from_segments(sub_m3u8.segments)
            
            if total_duration:
                for v in tracks_obj.videos:
                    v.duration = total_duration
                    if fps:
                        v.fps = fps
                    if v.bitrate:
                        v.size = int((float(v.bitrate) * total_duration) / 8)
                        
                for a in tracks_obj.audios:
                    a.duration = total_duration
                    if a.bitrate:
                        a.size = int((float(a.bitrate) * total_duration) / 8)

            if not has_encryption and sub_m3u8.keys:
                has_encryption = True
                for key in sub_m3u8.keys:
                    if key.method and key.method.upper() in ("SAMPLE-AES", "SAMPLE-AES-CTR"):
                        keyformat = key.keyformat
                        if keyformat and "edef8ba9-79d6-4ace-a3c8-27dcd51d21ed" in keyformat:
                            if not pssh and key.uri and "base64," in key.uri:
                                try:
                                    pssh_raw = key.uri.split("base64,")[-1]
                                    pssh_data = base64.b64decode(pssh_raw)
                                    try:
                                        pssh = Box.parse(pssh_data)
                                    except Exception:
                                        pssh = Box.parse(Box.build(dict(
                                            type=b"pssh", version=0, flags=0, system_ID=Cdm.uuid, init_data=pssh_data
                                        )))
                                except Exception as e:
                                    log.debug(f"Failed to decode Widevine PSSH from sub-manifest: {e}")
                        
                        if not pr_pssh and keyformat and "9a04f079-9840-4286-ab92-e65be0885f95" in keyformat:
                            if key.uri and "base64," in key.uri:
                                pr_pssh = key.uri.split("base64,")[-1]

                if has_encryption:
                    default_scheme = EncryptionScheme.WIDEVINE if pssh else EncryptionScheme.PLAYREADY if pr_pssh else EncryptionScheme.SAMPLE_AES
                    for track in tracks_obj:
                        track.encrypted = True
                        track.encryption_scheme = default_scheme
                        if isinstance(track.extra, dict):
                            if pssh and not track.extra.get("master_pssh"):
                                track.extra["master_pssh"] = pssh
                            if pr_pssh and not track.extra.get("master_pr_pssh"):
                                track.extra["master_pr_pssh"] = pr_pssh
                        else:
                            track.extra = {"master_pssh": pssh, "master_pr_pssh": pr_pssh}
                            
        except Exception as e:
            log.warning(f"Failed to probe HLS sub-manifest for duration/fps: {e}")

    return tracks_obj

def _safe_get_codec(stream_info):
    """Safely extract codec from stream_info, handling None values."""
    try:
        if hasattr(stream_info, 'codecs') and stream_info.codecs:
            return stream_info.codecs.split(",")[0].split(".")[0]
        return "h264"
    except (AttributeError, TypeError, IndexError):
        return "h264"

def _safe_get_resolution(stream_info):
    """Safely extract resolution from stream_info, handling None values."""
    try:
        if hasattr(stream_info, 'resolution') and stream_info.resolution:
            return stream_info.resolution
        return (0, 0)
    except (TypeError, AttributeError):
        return (0, 0)

def _safe_get_frame_rate(stream_info):
    """Safely extract frame rate from stream_info, handling None values."""
    try:
        if hasattr(stream_info, 'frame_rate') and stream_info.frame_rate:
            return stream_info.frame_rate
        return None
    except (TypeError, AttributeError):
        return None

def _safe_get_video_range(stream_info):
    """Safely extract video range from stream_info, handling None values."""
    try:
        if hasattr(stream_info, 'video_range') and stream_info.video_range:
            return stream_info.video_range.strip('"')
        return "SDR"
    except (TypeError, AttributeError):
        return "SDR"

def _safe_get_bitrate(stream_info):
    """Safely extract bitrate from stream_info, handling None values."""
    try:
        if hasattr(stream_info, 'average_bandwidth') and stream_info.average_bandwidth:
            return stream_info.average_bandwidth
        if hasattr(stream_info, 'bandwidth') and stream_info.bandwidth:
            return stream_info.bandwidth
        return 0
    except (TypeError, AttributeError):
        return 0

def _safe_get_audio_codec(media):
    """Safely extract audio codec from media entry."""
    try:
        if hasattr(media, 'codecs') and media.codecs:
            return media.codecs.split(",")[0].split(".")[0]
        if hasattr(media, 'group_id') and media.group_id:
            return media.group_id.replace("audio-", "").split("-")[0].split(".")[0]
        return "aac"
    except (AttributeError, TypeError, IndexError):
        return "aac"

def _is_dv(codec_str):
    """Check if codec indicates Dolby Vision."""
    try:
        if codec_str:
            return codec_str.split(".")[0] in ("dvhe", "dvh1")
        return False
    except (AttributeError, IndexError):
        return False
        
def _infer_fps_from_segments(segments):
    if not segments:
        return None
    
    durations = [seg.duration for seg in segments if seg.duration and seg.duration > 0]
    if not durations:
        return None
    
    avg_duration = sum(durations) / len(durations)
    
    for fps in [23.976, 24.0, 25.0, 29.97, 30.0, 50.0, 59.94, 60.0]:
        frames = avg_duration * fps
        if abs(frames - round(frames)) < 0.15:
            return fps
    
    return None        
```

### `wpgskd\core\manifests\ism.py`

```python
import asyncio
import hashlib
import logging
import urllib.parse
from typing import Optional

import requests
from langcodes import Language
from langcodes.tag_parser import LanguageTagError

from wpgskd.config import directories
from wpgskd.core.tracks import AudioTrack, TextTrack, Track, Tracks, VideoTrack
from wpgskd.core.io import aria2c
from wpgskd.core.xml import load_xml

log = logging.getLogger("ISMParser")

def _probe_ism_fps(url, session, timescale=10000000):
    try:
        s = session or requests
        res = s.get(url, timeout=10)
        res.raise_for_status()
        data = res.content
        
        def find_box_pos(data, target, start=0):
            pos = start
            while pos < len(data) - 8:
                size = int.from_bytes(data[pos:pos+4], 'big')
                btype = data[pos+4:pos+8]
                if size == 0: break
                if btype == target:
                    return pos, size
                if size < 8: break
                pos += size
            return -1, 0
            
        moof_pos, moof_size = find_box_pos(data, b'moof')
        if moof_pos == -1: return None
        
        traf_pos, traf_size = find_box_pos(data, b'traf', moof_pos + 8)
        if traf_pos == -1: return None
        
        trun_pos, trun_size = find_box_pos(data, b'trun', traf_pos + 8)
        if trun_pos == -1: return None
        
        version = data[trun_pos + 8]
        flags = int.from_bytes(data[trun_pos + 9 : trun_pos + 12], 'big')
        sample_count = int.from_bytes(data[trun_pos + 12 : trun_pos + 16], 'big')
        
        offset = trun_pos + 16
        if flags & 0x000001:  # data_offset_present
            offset += 4
        if flags & 0x000004:  # first_sample_flags_present
            offset += 4
            
        if flags & 0x000100:  # sample_duration_present
            total_duration = 0
            for _ in range(sample_count):
                total_duration += int.from_bytes(data[offset : offset + 4], 'big')
                offset += 4
                if flags & 0x000200:  # sample_size_present
                    offset += 4
                if flags & 0x000400:  # sample_flags_present
                    offset += 4
                if flags & 0x000800:  # sample_composition_time_present
                    offset += 4 if version == 0 else 8
            if total_duration > 0:
                fps = (sample_count * timescale) / total_duration
                return round(fps, 3)
                
        tfhd_pos, tfhd_size = find_box_pos(data, b'tfhd', traf_pos + 8)
        if tfhd_pos != -1:
            tfhd_flags = int.from_bytes(data[tfhd_pos + 9 : tfhd_pos + 12], 'big')
            tfhd_offset = tfhd_pos + 16 
            
            if tfhd_flags & 0x000001:  
                tfhd_offset += 8
            if tfhd_flags & 0x000002: 
                tfhd_offset += 4
                
            if tfhd_flags & 0x000008: 
                default_dur = int.from_bytes(data[tfhd_offset : tfhd_offset + 4], 'big')
                if default_dur > 0:
                    return round(timescale / default_dur, 3)
                    
    except Exception as e:
        log.warning(f"Failed to probe ISM FPS via raw bytes: {e}")
    return None

def parse(url: str = None, data: str = None, source: str = None, session: requests.Session = None, downloader: str = None) -> Tracks:
    if not data:
        if downloader is None:
            r = (session or requests).get(url)
            url = r.url  
            data = r.content
        elif downloader == "aria2c":
            out = directories.temp / url.split("/")[-1]
            asyncio.run(aria2c((url, out)))
            data = out.read_bytes()
            out.unlink(missing_ok=True)
        else:
            raise ValueError(f"Unsupported downloader: {downloader}")

    root = load_xml(data)
    if root.tag != "SmoothStreamingMedia":
        raise ValueError("Non-ISM document provided to ISM parser")

    tracks = []
    base_url = url
    duration = int(root.attrib.get("Duration", 0))
    root_timescale = int(root.get("TimeScale", 10000000))
    duration_sec = duration / root_timescale if root_timescale else 0
    
    if session is None:
        session = requests.Session()

    for stream_index in root.findall("StreamIndex"):
        stream_fps = None
        fps_probed = False    
        for ql in stream_index.findall("QualityLevel"):
            content_type = stream_index.get("Type")
            if not content_type:
                raise ValueError("No content type value could be found")
                
            codec = ql.get("FourCC")
            if codec == "TTML":
                codec = "STPP"

            track_lang = None
            if lang := (stream_index.get("Language") or "").strip():
                try:
                    t = Language.get(lang.split("-")[0])
                    if t == Language.get("und") or not t.is_valid():
                        raise LanguageTagError()
                except LanguageTagError:
                    pass
                else:
                    track_lang = Language.get(lang)

            protections = root.xpath(".//ProtectionHeader")
            pr_protections = [
                x for x in protections
                if (x.get("SystemID") or "").lower() == "9a04f079-9840-4286-ab92-e65be0885f95"
            ]
            protections = pr_protections
            encrypted = bool(protections)
            pssh = None
            pr_pssh = None
            kid = None
            
            if pr_protections:
                import base64
                import re
                from uuid import UUID
                for protection in pr_protections:
                    pr_pssh_text = "".join(protection.itertext())
                    if pr_pssh_text:
                        pr_pssh = pr_pssh_text
                        try:
                            raw_bytes = base64.b64decode(pr_pssh_text)
                            clean_str = raw_bytes.replace(b'\x00', b'').decode('utf-8', errors='ignore')
                            kid_match = re.search(r'<KID>([a-zA-Z0-9+/=]+)</KID>', clean_str)
                            if kid_match:
                                kid_bytes = base64.b64decode(kid_match.group(1))
                                if len(kid_bytes) == 16:
                                    kid = UUID(bytes_le=kid_bytes).hex
                        except Exception:
                            pass
                        break

            track_url = []
            fragment_ctx = {
                "time": 0,
            }
            stream_fragments = stream_index.findall("c")
            for stream_fragment_index, stream_fragment in enumerate(stream_fragments):
                fragment_ctx["time"] = int(stream_fragment.get("t", fragment_ctx["time"]))
                fragment_repeat = int(stream_fragment.get("r", 1))
                fragment_ctx["duration"] = int(stream_fragment.get("d"))
                
                if not fragment_ctx["duration"]:
                    try:
                        next_fragment_time = int(stream_index[stream_fragment_index + 1].attrib["t"])
                    except IndexError:
                        next_fragment_time = duration
                    fragment_ctx["duration"] = (next_fragment_time - fragment_ctx["time"]) / fragment_repeat
                    
                for _ in range(fragment_repeat):
                    track_url.append(
                        urllib.parse.urljoin(
                            base_url, stream_index.get("Url").format_map({
                                "bitrate": ql.get("Bitrate"),
                                "start time": str(fragment_ctx["time"]),
                            }),
                        )
                    )
                    fragment_ctx["time"] += fragment_ctx["duration"]

            if content_type == "video" and not fps_probed and track_url:
                stream_name = stream_index.get("Name") or "video"
                log.info(f" + Probing FPS from first fragment for stream: {stream_name}")
                stream_fps = _probe_ism_fps(track_url[0], session, root_timescale)
                fps_probed = True
                if stream_fps:
                    log.info(f" + Detected FPS: {stream_fps}")
                else:
                    log.warning(" + Could not detect FPS from fragment.")

            track_id = hashlib.md5(
                f"{codec}-{track_lang}-{ql.get('Bitrate') or 0}-{ql.get('Index') or 0}".encode(),
            ).hexdigest()

            if content_type == "video":
                vt = VideoTrack(
                    id_=track_id,
                    source=source,
                    url=track_url,
                    codec=codec or "",
                    language=track_lang,
                    bitrate=ql.get("Bitrate"),
                    width=int(ql.get("MaxWidth") or 0) or stream_index.get("MaxWidth"),
                    height=int(ql.get("MaxHeight") or 0) or stream_index.get("MaxHeight"),
                    fps=stream_fps,
                    hdr10=False,
                    hlg=False,
                    dv=(codec and codec.lower() in ("dvhe", "dvh1")),
                    descriptor=Track.Descriptor.ISM,
                    encrypted=encrypted,
                    pr_pssh=pr_pssh,
                    pssh=pssh,
                    kid=kid,
                    duration=duration_sec,
                    extra=(ql, stream_index, root),
                )
                vt.smooth = True
                tracks.append(vt)

            elif content_type == "audio":
                at = AudioTrack(
                    id_=track_id,
                    source=source,
                    url=track_url,
                    codec=codec or "",
                    language=track_lang,
                    bitrate=ql.get("Bitrate"),
                    channels=None,
                    descriptor=Track.Descriptor.ISM,
                    encrypted=encrypted,
                    pr_pssh=pr_pssh,
                    pssh=pssh,
                    kid=kid,
                    duration=duration_sec,
                    extra=(ql, stream_index, root),
                )
                at.smooth = True
                tracks.append(at)

            elif content_type == "text":
                tt = TextTrack(
                    id_=track_id,
                    source=source,
                    url=track_url,
                    codec=codec or "ttml",
                    language=track_lang,
                    descriptor=Track.Descriptor.ISM,
                    encrypted=encrypted,
                    pr_pssh=pr_pssh,
                    pssh=pssh,
                    kid=kid,
                    duration=duration_sec,
                    extra=(ql, stream_index, root),
                )
                tt.smooth = True
                tracks.append(tt)

    tracks_obj = Tracks()
    tracks_obj.add(tracks, warn_only=True)

    return tracks_obj
```

### `wpgskd\core\manifests\m3u8.py`

```python
import base64
import logging
from typing import List, Optional, Tuple, Any
import requests
import m3u8

from wpgskd.core.utilities import Cdm
from wpgskd.vendor.pymp4.parser import Box
from wpgskd.constants import EncryptionScheme

log = logging.getLogger("M3U8Parser")

def parse_media_playlist(url: str, session: requests.Session = None) -> dict:
    if not session:
        session = requests.Session()

    result = {
        "pssh": None,
        "pr_pssh": None,
        "kid": None,
        "aes_key_uri": None,
        "aes_iv": None,
        "init_url": None,
        "segments": []
    }

    try:
        res = session.get(url)
        res.raise_for_status()
        playlist = m3u8.loads(res.text, uri=url)
    except Exception as e:
        log.error(f"Failed to fetch/parse M3U8 playlist {url}: {e}")
        return result

    if playlist.segment_map:
        seg_map = playlist.segment_map
        init_uri = None
        if isinstance(seg_map, dict):
            init_uri = seg_map.get("uri")
        elif hasattr(seg_map, "uri"):
            init_uri = seg_map.uri
            
        if init_uri:
            result["init_url"] = init_uri if init_uri.startswith("http") else f"{playlist.base_uri}{init_uri}"

    for segment in playlist.segments:
        result["segments"].append(segment.absolute_uri)

    keys = playlist.session_keys or playlist.keys
    if not keys:
        return result

    widevine_urn = "urn:uuid:edef8ba9-79d6-4ace-a3c8-27dcd51d21ed"

    for key in keys:
        if not key or not key.method:
            continue
            
        method = key.method.upper()
        
        if method in ("SAMPLE-AES", "SAMPLE-AES-CTR") and key.keyformat and key.keyformat.lower() == widevine_urn:
            if key.uri and "base64," in key.uri:
                pssh_b64 = key.uri.split("base64,")[-1]
                try:
                    pssh_data = base64.b64decode(pssh_b64)
                    try:
                        result["pssh"] = Box.parse(pssh_data)
                    except Exception:
                        result["pssh"] = Box.parse(Box.build(dict(
                            type=b"pssh", version=0, flags=0, system_ID=Cdm.uuid, init_data=pssh_data
                        )))
                except Exception as e:
                    log.debug(f"Failed to decode Widevine PSSH from M3U8: {e}")


        elif method in ("SAMPLE-AES", "SAMPLE-AES-CTR") and key.keyformat and "playready" in key.keyformat.lower():
            if key.uri and "base64," in key.uri:
                result["pr_pssh"] = key.uri.split("base64,")[-1]

        elif method == "SAMPLE-AES" and key.keyformat and "apple" in key.keyformat.lower():
            result["aes_key_uri"] = key.uri

        elif method == "AES-128":
            result["aes_key_uri"] = key.absolute_uri
            if key.iv:
                result["aes_iv"] = bytes.fromhex(key.iv.replace("0x", ""))
            else:
                pass

    return result


def fetch_pssh_and_kid_from_m3u8(url: str, session: requests.Session = None) -> Tuple[Optional[Any], Optional[str]]:
    data = parse_media_playlist(url, session)
    
    pssh = data.get("pssh")
    kid = data.get("kid")
    
    if (not pssh or not kid) and data.get("init_url"):
        try:
            from wpgskd.core.manifests.map_init import extract_pssh_and_kid
            if not session:
                session = requests.Session()
            resp = session.get(data["init_url"], stream=True)
            chunk = next(resp.iter_content(20000), b"")
            pssh_list, kid_hex = extract_pssh_and_kid(chunk)
            if not pssh and pssh_list:
                pssh = pssh_list[0]
            if not kid and kid_hex:
                kid = kid_hex
        except Exception as e:
            log.debug(f"Failed to extract PSSH/KID from init.mp4 ({data['init_url']}): {e}")
            
    return pssh, kid

def fetch_aes_keys_from_m3u8(url: str, session: requests.Session = None) -> Tuple[Optional[str], Optional[bytes]]:
    data = parse_media_playlist(url, session)
    return data.get("aes_key_uri"), data.get("aes_iv")
```

### `wpgskd\core\manifests\map_init.py`

```python
import logging
import base64
from typing import Optional, Tuple, List
from uuid import UUID

from wpgskd.vendor.pymp4.parser import Box
from pywidevine.license_protocol_pb2 import WidevinePsshData

log = logging.getLogger("MapInit")

def extract_pssh_and_kid(data: bytes) -> Tuple[List[bytes], Optional[str]]:
    pssh_list = []
    kid_hex = None
    
    try:
        for box in _iterate_boxes(data, b"moov"):
            for tenc in _find_boxes(box, b"tenc"):
                if hasattr(tenc, 'key_ID') and tenc.key_ID:
                    kid_hex = tenc.key_ID.hex
                    break
            
            for pssh in _find_boxes(box, b"pssh"):
                if hasattr(pssh, 'init_data') and pssh.init_data:
                    pssh_list.append(Box.build(pssh))
                    
            if kid_hex or pssh_list:
                break
                
    except Exception as e:
        log.debug(f"Failed to parse MP4 boxes for PSSH/KID: {e}")
        
    return pssh_list, kid_hex

def parse_widevine_pssh(pssh_data: bytes) -> Tuple[Optional[bytes], Optional[str]]:
    try:
        box = Box.parse(pssh_data)
        if hasattr(box, 'init_data') and box.init_data:
            cenc_header = WidevinePsshData()
            cenc_header.ParseFromString(box.init_data)
            if cenc_header.key_id:
                kid = cenc_header.key_id[0]
                try:
                    int(kid, 16)
                    kid_hex = kid.decode().lower()
                except ValueError:
                    kid_hex = kid.hex().lower()
                return box, kid_hex
            return box, None
    except Exception:
        pass
    return None, None

def _iterate_boxes(data: bytes, box_type: bytes):
    offset = 0
    while offset + 8 <= len(data):
        try:
            size = int.from_bytes(data[offset:offset+4], "big")
            btype = data[offset+4:offset+8]
            if size < 8: break
            
            if btype == box_type:
                yield data[offset:offset+size]
                
            offset += size
        except Exception:
            offset += 8

def _find_boxes(data: bytes, box_type: bytes):
    offset = 0
    while offset + 8 <= len(data):
        try:
            size = int.from_bytes(data[offset:offset+4], "big")
            btype = data[offset+4:offset+8]
            if size < 8 or offset + size > len(data): break
            
            if btype == box_type:
                box = Box.parse(data[offset:offset+size])
                yield box
                
            offset += size
        except Exception:
            offset += 8
```

### `wpgskd\core\tracks\__init__.py`

```python
from wpgskd.core.tracks.tracks import Track, TextTrack, Tracks
from wpgskd.core.tracks.video import VideoTrack
from wpgskd.core.tracks.audio import AudioTrack
from wpgskd.core.tracks.title import Title, Titles
from wpgskd.core.tracks.menu import MenuTrack
from wpgskd.core.tracks.hdgrange import DynamicRange, detect_dynamic_range
```

### `wpgskd\core\tracks\audio.py`

```python
import math
from typing import Optional
from wpgskd.core.tracks.tracks import Track

AUDIO_CODEC_MAP = {
    "E-AC-3": "DD+",
    "E-AC-3 JOC": "DD+ Atmos",
    "AC-3": "DD",
    "AAC": "AAC",
    "AAC LC": "AAC",
    "FLAC": "FLAC",
    "Opus": "Opus",
    "DTS": "DTS",
    "DTS-HD": "DTS-HD",
    "DTS-HD MA": "DTS-HD.MA",
    "DTS XLL": "DTS-HD.MA",
    "MLP FBA": "TrueHD",
    "MLP FBA 16-ch": "TrueHD Atmos",
}

class AudioTrack(Track):
    def __init__(self, *args, bitrate: int, channels: Optional[str] = None,
                 descriptive: bool = False, atmos: bool = False, 
                 mpd_representation_id: Optional[str] = None, **kwargs):
        super().__init__(*args, **kwargs)
        self.bitrate = int(math.ceil(float(bitrate))) if bitrate else None
        self.channels = self.parse_channels(channels) if channels else None
        self.descriptive = bool(descriptive)
        self.atmos = bool(atmos)
        self.mpd_representation_id = mpd_representation_id

    @staticmethod
    def parse_channels(channels: str) -> str:
        if channels in ["A000", "a000"]: return "2.0"
        if channels in ["F801", "f801"]: return "5.1"
        try:
            ch = str(float(channels))
            if ch == "6.0": return "5.1"
            return ch
        except ValueError:
            return str(channels)

    def get_codec_display(self) -> str:
        if not self.codec:
            return "Unknown"
            
        codec_str = str(self.codec)
        codec_lower = codec_str.lower()
        
        display_name = codec_str
        
        if codec_str in AUDIO_CODEC_MAP:
            display_name = AUDIO_CODEC_MAP[codec_str]
        elif "ec-3" in codec_lower or "eac3" in codec_lower:
            display_name = "DDP"
        elif "ac-3" in codec_lower or "ac3" in codec_lower:
            display_name = "DD"
        elif "mp4a" in codec_lower or "aac" in codec_lower:
            display_name = "AAC"
        elif "opus" in codec_lower:
            display_name = "Opus"
        elif "flac" in codec_lower:
            display_name = "FLAC"
        elif "dts" in codec_lower:
            display_name = "DTS"
            
        if self.atmos and "Atmos" not in display_name:
            display_name += " Atmos"
            
        return display_name

    def get_track_name(self) -> Optional[str]:
        track_name = super().get_track_name() or ""
        flag = "Descriptive" if self.descriptive else ""
        if flag:
            if track_name:
                flag = f" ({flag})"
            track_name += flag
        return track_name or None

    def __str__(self):
        dur_sec = self.duration_seconds()
        size_bytes = self.size if self.size else self.computed_size_bytes()
        size_str = self.format_size_compact(size_bytes) if size_bytes else None
        dur_str = self.format_hms(dur_sec) if dur_sec else None
        
        codec_display = self.get_codec_display()
        if self.atmos and "Atmos" not in codec_display:
            codec_display = f"{codec_display} Atmos"
            
        return " | ".join([x for x in [
            "├─ AUD",
            codec_display,
            f"{self.channels}" if self.channels else None,
            f"{self.bitrate // 1000 if self.bitrate else '?'} kb/s",
            f"{self.language}",
            " ".join([self.get_track_name() or "", "[Original]" if self.is_original_lang else ""]).strip(),
            size_str,
            dur_str
        ] if x])
```

### `wpgskd\core\tracks\hdgrange.py`

```python
from enum import Enum
from typing import Any

class DynamicRange(Enum):
    SDR = "SDR"
    HDR10 = "HDR10"
    HDR10PLUS = "HDR10+"
    DV = "DV"
    HLG = "HLG"

def detect_dynamic_range(track: Any) -> DynamicRange:
    if getattr(track, 'dv', False):
        if getattr(track, 'hdr10', False):
            if getattr(track, 'dvhdr', False):
                return DynamicRange.HDR10
            return DynamicRange.DV
        return DynamicRange.DV
    if getattr(track, 'hdr10', False):
        return DynamicRange.HDR10
    if getattr(track, 'hlg', False):
        return DynamicRange.HLG
    return DynamicRange.SDR
```

### `wpgskd\core\tracks\menu.py`

```python
import re
from typing import Any, Optional

class MenuTrack:
    line_1 = re.compile(r"^CHAPTER(?P<number>\d+)=(?P<timecode>[\d\\.]+)$")
    line_2 = re.compile(r"^CHAPTER(?P<number>\d+)NAME=(?P<title>[\d\\.]+)$")

    def __init__(self, number: int, title: str, timecode: str):
        self.id = f"chapter-{number}"
        self.number = number
        self.title = title
        if "." not in timecode:
            timecode += ".000"
        self.timecode = timecode

    def __bool__(self):
        return bool(self.number and self.number >= 0 and self.title and self.timecode)

    def __repr__(self):
        return "CHAPTER{num}={time}\nCHAPTER{num}NAME={name}".format(
            num=f"{self.number:02}", time=self.timecode, name=self.title
        )

    def __str__(self):
        return " | ".join([
            "├─ CHP",
            f"[{self.number:02}]",
            self.timecode,
            self.title
        ])

    @classmethod
    def loads(cls, data: str) -> 'MenuTrack':
        lines = [x.strip() for x in data.strip().splitlines(keepends=False)]
        if len(lines) > 2:
            return MenuTrack.loads("\n".join(lines))
        one, two = lines

        one_m = cls.line_1.match(one)
        two_m = cls.line_2.match(two)
        if not one_m or not two_m:
            raise SyntaxError(f"An unexpected syntax error near:\n{one}\n{two}")

        one_str, timecode = one_m.groups()
        two_str, title = two_m.groups()
        one_num, two_num = int(one_str.lstrip("0")), int(two_str.lstrip("0"))

        if one_num != two_num:
            raise SyntaxError(f"The chapter numbers ({one_num},{two_num}) does not match.")
        if not timecode:
            raise SyntaxError("The timecode is missing.")
        if not title:
            raise SyntaxError("The title is missing.")

        return cls(number=one_num, title=title, timecode=timecode)

    @classmethod
    def load(cls, path: str) -> 'MenuTrack':
        with open(path, encoding="utf-8") as fd:
            return cls.loads(fd.read())

    def dumps(self) -> str:
        return repr(self)

    def dump(self, path: str):
        with open(path, "w", encoding="utf-8") as fd:
            return fd.write(self.dumps())

    @staticmethod
    def format_duration(seconds: float) -> str:
        minutes, seconds = divmod(seconds, 60)
        hours, minutes = divmod(minutes, 60)
        return f"{hours:02.0f}:{minutes:02.0f}:{seconds:06.3f}"
```

### `wpgskd\core\tracks\subtitles.py`

```python
import os
import re
import io
import logging
import math
import datetime
import unicodedata
import xml.etree.ElementTree as ET
from pathlib import Path
from collections import UserList, deque
from typing import Optional, List, Dict, Any, Tuple
from io import BytesIO
from functools import partial
import html

import srt
from srt import Subtitle

try:
    import tinycss
    from langcodes import Language
except ImportError:
    tinycss = None
    Language = None

from wpgskd.vendor.pymp4.parser import MP4
from wpgskd.vendor.pymp4.util import BoxUtil

log = logging.getLogger("Subtitles")

class SubRipFile(UserList):
    def __init__(self, data: list[srt.Subtitle] | None = None):
        self.data: list[srt.Subtitle] = data or []

    @classmethod
    def from_string(cls, source: str):
        return cls(list(srt.parse(source, ignore_errors=True)))

    def clean_indexes(self):
        self.data = list(srt.sort_and_reindex(self.data))

    def offset(self, offset: datetime.timedelta):
        for line in self.data:
            line.start += offset
            line.end += offset

    def export(self, eol: str | None = None) -> str:
        return srt.compose(self.data, eol=eol)

    def save(self, path: Path, encoding: str = 'utf-8-sig', eol: str | None = None):
        with path.open(mode='wb') as fp:
            fp.write(srt.compose(self.data, eol=eol).encode(encoding))

    def __eq__(self, other):
        if not isinstance(other, SubRipFile):
            raise NotImplementedError
        return self.export(eol='\n') == other.export(eol='\n')

def timestamp_from_ms(duration: float | int) -> str:
    seconds, miliseconds = divmod(float(duration), 1000)
    minutes, seconds = divmod(seconds, 60)
    hours, minutes = divmod(minutes, 60)
    return "%02d:%02d:%02d.%03d" % (hours, minutes, seconds, miliseconds)

def ms_from_timestamp(timestamp: str) -> int:
    timestamp = re.sub(r'[;\.\,]', r':', timestamp.replace('T:', ''))
    hours, minutes, seconds, miliseconds = map(int, timestamp.split(':'))
    miliseconds += hours * 3600000
    miliseconds += minutes * 60000
    miliseconds += seconds * 1000
    return miliseconds

def timedelta_from_timestamp(timestamp: str) -> datetime.timedelta:
    return datetime.timedelta(seconds=ms_from_timestamp(timestamp) / 1000)

def timedelta_from_ms(duration: float | int) -> datetime.timedelta:
    return datetime.timedelta(seconds=duration / 1000)

def line_duration(line: Subtitle):
    return abs(line.end - line.start)

TAGS = r'[<{][/\\]?[a-z0-9.]+[}>]'
POSITION_TAGS = r'^{\\an[0-9]}'
FRONT_OPTIONAL_TAGS_WITH_HYPHEN = rf'^\s*({TAGS})?\s*(-)?\s*({TAGS})?\s*'
TIME_LOOKAHEAD = r'(?![0-9]{2})'

SPEAKER = rf'({FRONT_OPTIONAL_TAGS_WITH_HYPHEN})\s*(Mc[A-Z][a-zA-Z]+|[A-Z0-9\&\[\]\.#\' ]+\s*|[A-Z][a-z]+):{TIME_LOOKAHEAD} ?'
SPEAKER_PARENTHESES = rf'({FRONT_OPTIONAL_TAGS_WITH_HYPHEN})\s*(?:[A-Z0-9\&\[\]\.#\' ]+\s*|[A-Z][a-z]+)(?: \([a-zA-Z ]+\)): ?'

FRONT_NOTES = r'(?:♪+\s+)'
BACK_NOTES = r'(?:\s+♪+)'

DESCRIPTION_BRACKET = r'\[(?:[^\]]|\s)*\]'
DESCRIPTION_PARENTHESES = r'\((?:[^\)]|\s)*\)'
FULL_LINE_DESCIRPTION_BRACKET = rf'^-?\s*{FRONT_NOTES}?\[[^\]]+\]{BACK_NOTES}?$'
NEW_LINE_DESCRIPTION_BRACKET = rf'^(?:{TAGS})?-?\s*{FRONT_NOTES}?{DESCRIPTION_BRACKET}(?:{TAGS})?{BACK_NOTES}?$'
FRONT_DESCRIPTION_BRACKET = rf'^(?:{SPEAKER}|{SPEAKER_PARENTHESES})?({FRONT_OPTIONAL_TAGS_WITH_HYPHEN}){DESCRIPTION_BRACKET}:?'
END_DESCRIPTION_BRACKET = rf'\s*{DESCRIPTION_BRACKET}\s*$'
FULL_LINE_DESCIRPTION_PARENTHESES = rf'^-?\s*{FRONT_NOTES}?\([^\)]+\){BACK_NOTES}?$'
NEW_LINE_DESCRIPTION_PARENTHESES = rf'^(?:{TAGS})?-?\s*{FRONT_NOTES}?{DESCRIPTION_PARENTHESES}{BACK_NOTES}?(?:{TAGS})?$'
FRONT_DESCRIPTION_PARENTHESES = rf'^({FRONT_OPTIONAL_TAGS_WITH_HYPHEN})(?:{SPEAKER}|{SPEAKER_PARENTHESES})?{DESCRIPTION_PARENTHESES}:?'
END_DESCRIPTION_PARENTHESES = rf'\s*{DESCRIPTION_PARENTHESES}:?\s*$'
INLINE_DESCRIPTION = r'(?:<[a-z]+>)?[\[(][A-Z]+[)\]](?:</[a-z]+>)?'

class BaseConverter:
    def from_file(self, file: Path) -> SubRipFile:
        with file.open(mode='rb') as stream:
            return self.parse(stream)

    def from_string(self, data: str) -> SubRipFile:
        return self.parse(BytesIO(data.encode('utf-8')))

    def from_bytes(self, data: bytes) -> SubRipFile:
        return self.parse(BytesIO(data))

    def parse(self, stream) -> SubRipFile:
        raise NotImplementedError

class WebVTTConverter(BaseConverter):
    def parse(self, stream) -> SubRipFile:
        srt = SubRipFile()
        looking_for_text = False
        looking_for_style = False
        text = []
        position = None
        line_number = 1
        styles = {}
        current_style = []
        css_parser = tinycss.make_parser('page3') if tinycss else None

        for line in stream:
            line = line.decode('utf-8').replace('\r\n', '\n').replace('\r', '\n').strip()
            if any(line.startswith(word) for word in ('WEBVTT', 'NOTE', '/*', 'X-TIMESTAMP-MAP')):
                continue

            if line == '':
                if looking_for_style and current_style and css_parser:
                    stylesheet = css_parser.parse_stylesheet('\n'.join(current_style))
                    for rule in stylesheet.rules:
                        ft = next((e for e in rule.selector if e.type == 'FUNCTION'), None)
                        if not ft: continue
                        name = next((t for t in ft.content if t.type == 'IDENT'), None)
                        if not name: continue
                        styles[name.value] = {}
                        for dec in rule.declarations:
                            styles[name.value][dec.name] = dec.value.as_css()
                    current_style = []
                    looking_for_style = False

                if not text:
                    continue

                srt[-1].content = '\n'.join(text)
                text = []
                looking_for_text = False

            elif 'STYLE' in line:
                looking_for_style = True
            elif looking_for_style:
                current_style.append(line)
            elif ' --> ' in line:
                parts = line.strip().split()
                position = self._get_position([p for p in parts[3:] if ':' in p])
                start, _, end, *_ = parts
                if start.count(':') == 1: start = f'00:{start}'
                if end.count(':') == 1: end = f'00:{end}'

                srt.append(Subtitle(index=line_number, start=timedelta_from_timestamp(start), end=timedelta_from_timestamp(end), content=''))
                looking_for_text = True
                line_number += 1
            elif looking_for_text:
                line = html.unescape(line)
                line = re.sub(r'<v\s+[^>]+>', '', line)
                if position is not None and position < 25:
                    line = '{\\an8}' + line
                    position = None
                text.append(line.strip())

        if text:
            srt[-1].content += '\n'.join(text)

        for line in srt:
            line.content = re.sub(r'<c.([a-zA-Z0-9]+)>([^<]+)<\/c>', 
                                  partial(self._replace_italics, styles=styles), line.content)
            line.content = re.sub(r'</?(?!/?i)[^>\s]+>', '', line.content)

        return srt

    @staticmethod
    def _get_position(cue_settings: list[str]) -> Optional[float]:
        if not cue_settings or cue_settings == ['None']: return None
        for key, val in (pos.split(':') for pos in cue_settings):
            if key == 'line' and (val := val.split(',')[0])[-1] == '%':
                return float(val[:-1])
        return None

    @staticmethod
    def _replace_italics(match: re.Match, styles: dict[str, dict[str, str]]) -> str:
        if (s := styles.get(match[1])) and s.get('font-style') == 'italic':
            return f'<i>{match[2]}</i>'
        return match[0]

class SMPTEConverter(BaseConverter):
    """DFXP/TTML/TTML2 subtitle converter"""
    def parse(self, stream) -> SubRipFile:
        data = stream.read().decode('utf-8-sig')
        if data.count('</tt>') == 1:
            return _SMPTEConverter(data).srt

        smpte_subs = [s + '</tt>' for s in data.strip().split('</tt>') if s]
        srt = SubRipFile([])
        for sub in smpte_subs:
            srt.extend(_SMPTEConverter(sub).srt)
        return srt

class _SMPTEConverter:
    def __init__(self, data: str):
        self.logger = logging.getLogger(__name__)
        
        data = re.sub(r'<\?xml[^>]*\?>', '', data)
        data = re.sub(r'\sxmlns(?::[a-zA-Z\-]+)?="[^"]*"', '', data)
        data = data.replace('ttp:', '').replace('tts:', '').replace('xml:', '')
        
        try:
            self.root = ET.fromstring(data)
            for elem in self.root.iter():
                if isinstance(elem.tag, str) and "}" in elem.tag:
                    elem.tag = elem.tag.split("}", 1)[1]
        except ET.ParseError as e:
            self.logger.error(f"TTML parse error: {e}")
            self.root = None

        self.srt = SubRipFile([])
        if self.root is None:
            return
            
        self.tickrate = int(self.root.get('tickRate', 0))
        self.frame_duration = 1
        if (rate := self.root.get('frameRate')) is not None:
            try:
                num, denom = map(int, self.root.get('frameRateMultiplier', '1 1').split())
                framerate = (int(rate) * num) / denom
                self.frame_duration = (1 / framerate) * 1000
            except ValueError:
                pass

        self.italics = {}
        self.an8 = {}
        self.all_span_italics = 'fontStyle="italic"' not in data

        self._parse_styles()
        self._convert()

    def _convert(self):
        p_elements = self.root.findall(".//p")
        if not p_elements:
            p_elements = [
                e for e in self.root.iter()
                if isinstance(e.tag, str) and e.tag.split("}")[-1] == "p"
            ]

        if not p_elements:
            self.logger.warning("TTML parse: No <p> elements found in document.")
            return

        for num, line in enumerate(p_elements, 1):
            line_text = ''
            begin = line.get('begin')
            end = line.get('end')
            if not begin or not end: continue

            try:
                if begin.endswith('t'): begin = self._convert_ticks(begin)
                elif begin.endswith('ms'): begin = timestamp_from_ms(begin[:-2])
                else: begin = self._parse_timestamp(begin)

                if end.endswith('t'): end = self._convert_ticks(end)
                elif end.endswith('ms'): end = timestamp_from_ms(end[:-2])
                else: end = self._parse_timestamp(end)
            except Exception as e:
                self.logger.warning(f"TTML parse: Failed to parse timestamp for line {num}: {e}")
                continue

            srt_line = Subtitle(index=num, start=timedelta_from_timestamp(begin), end=timedelta_from_timestamp(end), content='')
            line_text = self._parse_element(line)

            if self._is_italic(line) and line_text.strip():
                line_text = line_text.replace('<i>', '').replace('</i>', '')
                line_text = '<i>%s</i>' % line_text.strip()
            if self._is_an8(line) and line_text.strip():
                line_text = '{\\an8}%s' % line_text.strip()

            srt_line.content = line_text.strip().strip('\n')
            if srt_line.content:
                self.srt.append(srt_line)

    def _parse_styles(self):
        for style in self.root.findall('.//style'):
            sid = style.get('id')
            if sid: self.italics[sid] = self._is_italic(style)
        for region in self.root.findall('.//region'):
            rid = region.get('id')
            if rid: self.an8[rid] = self._is_an8(region)

    def _parse_element(self, element):
        element_text = ""
        if element.text:
            element_text += element.text

        for child in element:
            tag = child.tag.split("}")[-1] if isinstance(child.tag, str) else ""
            element_text += self._parse_element(child)

            if tag == "br":
                element_text += "\n"

            if child.tail:
                element_text += child.tail

        if self._is_italic(element) and element_text.strip():
            element_text = element_text.replace("<i>", "").replace("</i>", "")
            element_text = "<i>%s</i>" % element_text.strip()

        if self._is_an8(element) and element_text.strip():
            element_text = "{\\an8}%s" % element_text.strip()

        return element_text
        
    def _is_italic(self, element):
        if element is None: return False
        if element.get('fontStyle') == 'italic': return True
        style_id = element.get('style')
        if style_id and self.italics.get(style_id): return True
        tag = element.tag.split("}")[-1] if isinstance(element.tag, str) else ""

        if self.all_span_italics and tag == "span" and not element.attrib:
            return True
        return False

    def _is_an8(self, element):
        if element.get('displayAlign') == 'before': return True
        region_id = element.get('region')
        if region_id and self.an8.get(region_id): return True
        return False

    def _convert_ticks(self, ticks):
        ticks = int(ticks[:-1])
        offset = 1.0 / self.tickrate if self.tickrate else 0
        seconds = (offset * ticks) * 1000
        return timestamp_from_ms(seconds)

    def _parse_timestamp(self, timestamp):
        regex = r'([0-9]{2}):([0-9]{2}):([0-9]{2})[:\.,]?([0-9]{0,3})?'
        parsed = re.search(regex, timestamp)
        if not parsed: return "00:00:00.000"
        hours, minutes, seconds = int(parsed.group(1)), int(parsed.group(2)), int(parsed.group(3))
        miliseconds = 0
        if fraction := parsed.group(4):
            if timestamp[-len(fraction)-1] == ':':
                miliseconds = int(self.frame_duration * int(fraction))
            else:
                miliseconds = int(float(f"0.{fraction}") * 1000)
        return "%02d:%02d:%02d.%03d" % (hours, minutes, seconds, miliseconds)

class SAMIConverter(BaseConverter):
    def parse(self, stream) -> SubRipFile:
        return _SAMIConverter(stream.read().decode('utf-8-sig')).srt

class _SAMIConverter(html.parser.HTMLParser):
    def __init__(self, subtitle):
        super().__init__()
        self.lines = []
        self.tags = []
        self.srt = SubRipFile([])
        self.line_list = []
        self.feed(self._correct_tags(subtitle))
        self._convert()

    def handle_starttag(self, tag, attrs_org):
        attrs = {k: v for k, v in attrs_org}
        if tag == 'sync':
            self.lines.append({'text': '', **attrs})
        self.tags.append({'name': tag, 'attrs': attrs})

    def handle_data(self, data):
        if not self.tags: return
        last_tag = self.tags[-1]['name']
        if last_tag == 'br': self.lines[-1]['text'] += '\n'
        elif last_tag == 'i' and data.strip(): self.lines[-1]['text'] += f'<i>{data}</i>'
        elif last_tag != 'sync' and self.lines: self.lines[-1]['text'] += data

    def _convert(self):
        for line in self.lines:
            if not line.get('text', '').strip():
                end_time = float(line['start'])
                if self.line_list: self.line_list[-1]['end'] = end_time
                continue
            if not line.get('end'): line['end'] = float(line['start']) + 4000
            self.line_list.append({'start': float(line['start']), 'end': float(line['end']), 'content': line['text'].strip()})

        for num, line in enumerate(self.line_list):
            self.srt.append(Subtitle(index=num, start=timedelta_from_ms(line['start']), end=timedelta_from_ms(line['end']), content=line['content']))

    @staticmethod
    def _correct_tags(data):
        data = data.replace('<i/>', '<i>').replace(';>', '>').replace('<br>', '\n').replace('<br/>', '\n').replace('<br >', '\n')
        return data

class WVTTConverter(BaseConverter):
    def parse(self, stream) -> SubRipFile:
        sample_durations = deque()
        vtt_lines = []
        timescale = 0

        for box in MP4.parse(stream.read()):
            if box.type == b'moov':
                for mdhd in BoxUtil.find(box, b'mdhd'): timescale = mdhd.timescale; break
                for stsd in BoxUtil.find(box, b'stsd'):
                    wvtt = stsd.entries[0]
                    header = [box.config for box in wvtt.children if box.type == b'vttC'][0]
                    vtt_lines.append(f'{header}\n\n')
                    break
            if box.type == b'moof':
                start_offset = 0
                duration = 0
                for tfdt in BoxUtil.find(box, b'tfdt'): start_offset = tfdt.baseMediaDecodeTime; break
                for trun in BoxUtil.find(box, b'trun'):
                    for sample in trun.sample_info:
                        start_offset += sample.sample_composition_time_offsets or 0
                        duration += sample.sample_duration or 0
                        sample_durations.append({'start_ms': (start_offset / timescale) * 1000, 'end_ms': ((start_offset + duration) / timescale) * 1000})
            if box.type == b'mdat':
                for vtt_box in MP4.parse(box.data):
                    settings = next((box.settings for box in BoxUtil.find(vtt_box, b'sttg')), None)
                    cue_text = next((box.cue_text for box in BoxUtil.find(vtt_box, b'payl')), None)
                    try: sample_duration = sample_durations.popleft()
                    except IndexError: continue
                    start_ms = end_ms = sample_duration['end_ms']
                    end_ms = sample_duration['end_ms']
                    if vtt_box.type == b'vtte': continue
                    vtt_lines.append(f'{timestamp_from_ms(start_ms)} --> {timestamp_from_ms(end_ms)} {settings}\n{cue_text}\n\n')

        return WebVTTConverter().from_string(''.join(vtt_lines))

class ISMTConverter(BaseConverter):
    def parse(self, stream) -> SubRipFile:
        srt = SubRipFile([])
        for box in MP4.parse(stream.read()):
            if box.type == b'mdat':
                new = SMPTEConverter().from_bytes(box.data)
                if srt and new and srt[-1].start > new[0].start: new.offset(srt[-1].end)
                srt.extend(new)
        return srt

class BilibiliJSONConverter(BaseConverter):
    def parse(self, stream) -> SubRipFile:
        import json
        json_data = json.load(stream)
        srt = SubRipFile()
        for i, line in enumerate(json_data['body']):
            if line['location'] != 2:
                line['content'] = ('{\\an%s}' % line['location']) + line['content']
            srt.append(Subtitle(index=i, start=datetime.timedelta(seconds=line['from']), end=datetime.timedelta(seconds=line['to']), content=line['content']))
        return srt

class LegacyTTMLConverter:
    TOP_MARKER = '{\\an8}'

    def __init__(self, shift=0, source_fps=23.976, scale_factor=1, subtitle_language=None):
        self.shift = shift
        self.source_fps = source_fps
        self.scale_factor = scale_factor
        self.subtitle_language = subtitle_language
        self.entries = []
        self._tc = self._init_timestamp_converter()

    class _TimestampConverter:
        def __init__(self, frame_rate=23.976, tick_rate=1):
            self.frame_rate = frame_rate
            self.tick_rate = tick_rate

        def timeexpr_to_ms(self, time_expr):
            delims = ''.join([i for i in time_expr if not i.isdigit()])
            fn_map = {
                '::': self.frame_timestamp_to_ms, ':::': self.frame_timestamp_to_ms,
                '::.': self.fraction_timestamp_to_ms,
                'h': self.offset_hours_to_ms, 'm': self.offset_minutes_to_ms,
                's': self.offset_seconds_to_ms, 'ms': self.offset_ms_to_ms,
                't': self.offset_ticks_to_ms, 'f': self.offset_frames_to_ms
            }
            return fn_map.get(delims, lambda x: 0)(time_expr)

        def _hhmmss_to_ms(self, hh, mm, ss): return hh * 3600 * 1000 + mm * 60 * 1000 + ss * 1000
        def subrip_to_ms(self, ts):
            hh, mm, ss, ms = re.split(r'[:,]', ts)
            return int(int(hh) * 3.6e6 + int(mm) * 60000 + int(ss) * 1000 + int(ms))
        def ms_to_subrip(self, ms):
            hh = int(ms / 3.6e6); mm = int((ms % 3.6e6) / 60000); ss = int((ms % 60000) / 1000); ms = int(ms % 1000)
            return '{:02d}:{:02d}:{:02d},{:03d}'.format(hh, mm, ss, ms)
        def ms_to_ssa(self, ms):
            hh = int(ms / 3.6e6); mm = int((ms % 3.6e6) / 60000); ss = int((ms % 60000) / 1000); ms = int(ms % 1000)
            return '{:01d}:{:02d}:{:02d}.{:02d}'.format(hh, mm, ss, int(ms / 10))
        def frames_to_ms(self, frames): return int(int(frames) * (1000 / self.frame_rate))
        def offset_frames_to_ms(self, time): return int(int(float(time[:-1])) * (1000 / self.frame_rate))
        def offset_ticks_to_ms(self, time): return (1.0 / self.tick_rate * int(time[:-1])) * 1000
        def offset_hours_to_ms(self, time): return int(3.6e6 * float(time[:-1]))
        def offset_minutes_to_ms(self, time): return int(60 * 1000 * float(time[:-1]))
        def offset_seconds_to_ms(self, time): return int(1000 * float(time[:-1]))
        def offset_ms_to_ms(self, time): return int(time[:-2])
        def fraction_timestamp_to_ms(self, ts):
            hh, mm, ss, fraction = re.split(r'[:.]', ts)
            return self._hhmmss_to_ms(int(hh), int(mm), int(ss)) + int(fraction[:3])
        def frame_timestamp_to_ms(self, ts):
            hh, mm, ss, frames = [int(i) for i in ts.split('.')[0].split(':')]
            return self._hhmmss_to_ms(hh, mm, ss) + self.frames_to_ms(frames)

    def _init_timestamp_converter(self):
        return self._TimestampConverter(self.source_fps)

    def parse_ttml_from_string(self, doc: str):
        try:
            from defusedxml import minidom
        except ImportError:
            from xml.dom import minidom

        del self.entries[:]
        ttml_dom = minidom.parseString(doc.encode('utf-8'))
        tt_element = ttml_dom.getElementsByTagNameNS('*', 'tt')[0]
        
        if (ttp_val := getattr(tt_element.attributes.get('ttp:frameRate'), 'value', None)):
            self._tc.frame_rate = float(ttp_val)
        if (ttp_val := getattr(tt_element.attributes.get('ttp:tickRate'), 'value', None)):
            self._tc.tick_rate = int(ttp_val)

        lines = [i for i in ttml_dom.getElementsByTagNameNS('*', 'p') if 'begin' in i.attributes.keys()]
        for p in lines:
            ms_begin = self._tc.timeexpr_to_ms(p.attributes['begin'].value)
            ms_end = self._tc.timeexpr_to_ms(p.attributes['end'].value)
            dialogue = self._extract_dialogue(p.childNodes)
            position = 'top' if p.getAttribute('region') in self._get_top_regions(ttml_dom) else 'bottom'
            self.entries.append({'ms_begin': ms_begin, 'ms_end': ms_end, 'text': dialogue, 'position': position})
        
        if self.scale_factor != 1:
            for e in self.entries: e['ms_begin'] *= self.scale_factor; e['ms_end'] *= self.scale_factor
        if self.shift:
            for e in self.entries: e['ms_begin'] += self.shift; e['ms_end'] += self.shift

    @staticmethod
    def _get_top_regions(ttml_dom):
        top_regions = []
        for region in ttml_dom.getElementsByTagName('region'):
            if region.getAttribute('tts:displayAlign') == 'before':
                if rid := region.getAttribute('xml:id'): top_regions.append(rid)
        return top_regions

    def _extract_dialogue(self, nodes, styles=[]):
        dialogue = []
        for node in nodes:
            if node.nodeType == node.TEXT_NODE:
                text = re.sub(r'^\s{4,}', '', node.nodeValue.replace('\n', ''))
                fmt = '{ot}{f}{et}'.format(et='</i>', ot='<i>', f='{}')
                for style in styles: dialogue.append(fmt.format(text))
            elif node.localName == 'br': dialogue.append('\n')
            elif node.localName == 'span':
                if node.getAttribute('style') == 'italic' or node.parentNode.getAttribute('style') == 'AmazonDefaultStyle':
                    dialogue += self._extract_dialogue(node.childNodes, ['i'])
                else:
                    dialogue += self._extract_dialogue(node.childNodes, [])
        return ''.join(dialogue)

    def generate_srt(self) -> str:
        res = ''
        for i, e in enumerate(self.entries, 1):
            text = e['text'].replace("\n", "\r\n")
            if e['position'] == 'top': text = self.TOP_MARKER + text
            res += '{}\r\n{} --> {}\r\n{}\r\n\r\n'.format(i, self._tc.ms_to_subrip(e['ms_begin']), self._tc.ms_to_subrip(e['ms_end']), text)
        return res

    def generate_ssa(self) -> str:
        res = "[Script Info]\r\nScriptType: v4.00+\r\nPlayResX: 1280\r\nPlayResY: 720\r\n\r\n[V4+ Styles]\r\nFormat: Name,Fontname,Fontsize,PrimaryColour,BackColour,Bold,Italic,Alignment\r\nStyle: Default,Arial,50,&H00EEEEEE,&H40000000,0,0,2\r\n\r\n[Events]\r\nFormat: Layer,Start,End,Style,Name,MarginL,MarginR,MarginV,Effect,Text\r\n"
        for e in self.entries:
            text = e['text']
            text = re.sub(r'<i.*?>', '{\\\\i1}', text); text = re.sub(r'</i>', '{\\\\i0}', text)
            text = text.replace('\n', '\\\\N')
            if e['position'] == 'top': text = self.TOP_MARKER + text
            res += 'Dialogue: 0,{},{},Default,,0,0,0,,{}\r\n'.format(self._tc.ms_to_ssa(e['ms_begin']), self._tc.ms_to_ssa(e['ms_end']), text)
        return res

class BaseProcessor:
    def from_srt(self, srt: SubRipFile, language: str | None = None) -> Tuple[SubRipFile, bool]:
        return self.process(srt, language)
    def from_file(self, file: Path, language: str | None = None) -> Tuple[SubRipFile, bool]:
        with file.open(mode='r', encoding='utf-8') as stream: return self.from_string(stream.read(), language)
    def from_string(self, data: str, language: str | None = None) -> Tuple[SubRipFile, bool]:
        return self.process(SubRipFile.from_string(data), language)
    def process(self, srt: SubRipFile, language: str | None = None) -> Tuple[SubRipFile, bool]:
        raise NotImplementedError

class RTLFixer(BaseProcessor):
    RTL_LANGUAGES = ('ar', 'fa', 'he', 'ps', 'syc', 'ug', 'ur')
    RTL_CHAR = '\u202b'
    def process(self, srt, language=None):
        corrected = self._correct_subtitles(srt)
        return srt, corrected != srt
    def _correct_subtitles(self, srt):
        for line in srt:
            line.content = RTL_CHAR + line.content.replace("\n", f"\n{RTL_CHAR}")
        return srt

class CommonIssuesFixer(BaseProcessor):
    remove_gaps = True
    def process(self, srt, language=None):
        fixed = self._fix_time_codes(srt)
        corrected = self._correct_subtitles(fixed)
        if language and Language and Language.get(language).language in RTLFixer.RTL_LANGUAGES:
            corrected, _ = RTLFixer().process(corrected, language=language)
        return corrected, corrected != srt

    def _correct_subtitles(self, srt: SubRipFile) -> SubRipFile:
        def _fix_line(line):
            line = re.sub(r' {2,}', ' ', line)
            line = unicodedata.normalize('NFKC', line)
            line = line.replace(r'â™ª', '♪').replace(r'‐', r'-').replace(r'♫', r'♪')
            line = re.sub(r'^((?:{\\an8})?(?:<i>)?)(- ?)?[#\*]{1,}(?=\s+)', r'\1\2♪', line, flags=re.M)
            line = re.sub(r'(\{\\an[0-9]\}){1,}', r'{\\an8}', line)
            line = re.sub(r'</?(?!i>)[a-z]+>', '', line)
            line = re.sub(r'(<[a-z]>) {1,}', r'\1', line)
            line = re.sub(r'(<[a-z]>)\n', r'\n\1', line)
            line = re.sub(r'\n(</[a-z]>)', r'\1\n', line)
            line = re.sub(r"^(<i>|\{\\an8\})?-+(?='?[\w\"\[\(\<\{\.\$♪])", r"\1- ", line, flags=re.M)
            line = re.sub(r'(.*)([^\.\sA-Z][!\.;:?])(?<!(?:Mr|Ms)\.)(?<!Mrs\.)([A-Z][^.])', r'- \1\2\n- \3', line)
            return line.strip()

        for line in srt:
            for _ in range(2):
                line.content = html.unescape(line.content)
            for _ in range(2):
                line.content = _fix_line(line.content).strip()
                line.content = line.content.strip('\n')

        combined = self._combine_timecodes(srt)
        return self._remove_gaps(combined) if self.remove_gaps else combined

    def _combine_timecodes(self, srt: SubRipFile) -> SubRipFile:
        subs_copy = SubRipFile([])
        for line in srt:
            if not subs_copy: subs_copy.append(line); continue
            if line_duration(subs_copy[-1]) == line_duration(line) and subs_copy[-1].start == line.start and subs_copy[-1].end == line.end:
                if subs_copy[-1].content != line.content: subs_copy[-1].content += '\n' + line.content
            elif 0 < round((line.start - subs_copy[-1].end).total_seconds() * 1000) <= 85 and line.content.startswith(subs_copy[-1].content) and self.remove_gaps:
                subs_copy[-1].end = line.end; subs_copy[-1].content = line.content
            else:
                subs_copy.append(line)
        subs_copy.clean_indexes()
        return subs_copy or srt

    def _remove_gaps(self, srt: SubRipFile) -> SubRipFile:
        subs_copy = SubRipFile([])
        for line in srt:
            if not subs_copy: subs_copy.append(line); continue
            elif 1 < round((line.start - subs_copy[-1].end).total_seconds() * 1000) <= 85:
                line.start = subs_copy[-1].end
                subs_copy[-1].end -= datetime.timedelta(milliseconds=1)
                subs_copy.append(line)
            else: subs_copy.append(line)
        subs_copy.clean_indexes()
        return subs_copy or srt

    @staticmethod
    def _fix_time_codes(srt: SubRipFile) -> SubRipFile:
        offset = 0
        for line in srt:
            hours, _ = divmod(line.start.seconds, 3600)
            hours += line.start.days * 24
            if not offset and hours > 23: offset = hours
            if offset:
                line.start -= datetime.timedelta(hours=offset); line.end -= datetime.timedelta(hours=offset)
        return srt

class SDHStripper(BaseProcessor):
    def process(self, srt, language=None):
        stripped = [line for line in srt]
        stripped = self._clean_full_line_descriptions(stripped)
        stripped = self._clean_new_line_descriptions(stripped)
        stripped = self._clean_inline_descriptions(stripped)
        stripped = self._clean_speaker_names(stripped)
        stripped = self._strip_notes(stripped)
        stripped = self._remove_extra_hyphens(stripped)
        stripped = SubRipFile([line for line in stripped if line.content])
        stripped.clean_indexes()
        return stripped, stripped != srt

    def _clean_full_line_descriptions(self, srt):
        for line in srt:
            text = re.sub(TAGS, r'', line.content)
            for regex in (FULL_LINE_DESCIRPTION_BRACKET, FULL_LINE_DESCIRPTION_PARENTHESES):
                text = re.sub(regex, r'', text, flags=re.S).strip()
            if text: yield line

    def _clean_new_line_descriptions(self, srt):
        for line in srt:
            position = re.match(POSITION_TAGS, line.content.strip())
            for regex in (NEW_LINE_DESCRIPTION_BRACKET, NEW_LINE_DESCRIPTION_PARENTHESES):
                line.content = re.sub(regex, r'', line.content, flags=re.M).strip()
            if position and position[0] not in line.content: line.content = position[0] + line.content
            yield line

    def _clean_inline_descriptions(self, srt):
        for line in srt:
            line.content = re.sub(FRONT_DESCRIPTION_BRACKET, r'\10', line.content, flags=re.M)
            line.content = re.sub(FRONT_DESCRIPTION_PARENTHESES, r'\1', line.content, flags=re.M)
            for regex in (END_DESCRIPTION_BRACKET, END_DESCRIPTION_PARENTHESES, INLINE_DESCRIPTION):
                line.content = re.sub(regex, r'', line.content, flags=re.M).strip()
            yield line

    def _clean_speaker_names(self, srt):
        for line in srt:
            for regex in (SPEAKER_PARENTHESES, SPEAKER):
                line.content = re.sub(regex, r'\2\3', line.content, flags=re.M).strip()
            yield line

    def _strip_notes(self, srt):
        for line in srt:
            if not re.match(r'^♪+$', re.sub(r'\s*', r'', re.sub(TAGS, r'', line.content).strip())): yield line

    def _remove_extra_hyphens(self, srt):
        for line in srt:
            splits = len(re.findall(r'^(<i>|\{\\an8\})?-\s*', line.content, flags=re.M))
            if splits == 1: line.content = re.sub(r'^(<i>|\{\\an8\})?-\s*', r'\1', line.content.strip())
            yield line

class SubtitleProcessor:
    _SDH_PATTERNS = [
        r'\[[^\]]*\]', r'\([^\)]*\)', r'\{[^\}]*\}', r'<[^>]*>', r'♪[^♪]*♪', r'[\*_][^\*_]+[\*_]',
    ]

    @staticmethod
    def extract_mdat_text(data: bytes, codec: str) -> bytes:
        codec_lower = codec.lower()
        plain_text_codecs = {"vtt", "webvtt", "webvtt-lssdh-ios8", "ttml", "ttml2", "dfxp", "smpte"}
        if codec_lower in plain_text_codecs: return data

        collected = []
        try:
            offset = 0
            while offset + 8 <= len(data):
                box_size = int.from_bytes(data[offset:offset + 4], "big")
                box_type = data[offset + 4:offset + 8]
                if box_size < 8: break
                if box_type == b"mdat":
                    payload = data[offset + 8: offset + box_size]
                    if codec_lower in ["wvtt", "stpp"]:
                        cues_data = SubtitleProcessor._extract_wvtt_text_from_mdat(payload)
                        if cues_data and len(cues_data) > 10: collected.append(cues_data)
                    else:
                        clean = payload.lstrip(b"\x00").strip()
                        if clean and len(clean) > 10: collected.append(clean)
                offset += box_size
        except Exception as e:
            log.debug(f"Error extracting MDAT: {e}")

        if not collected: return data
        result = b"\n".join(collected)
        if b"WEBVTT" not in result and b"-->" in result:
            lines = result.split(b'\n')
            for i, line in enumerate(lines):
                if b"-->" in line: lines.insert(0, b"WEBVTT"); lines.insert(1, b""); result = b'\n'.join(lines); break
        return result.replace(b'\x00', b'')

    @staticmethod
    def convert_subtitle_to_srt(save_path: str, strip_sdh: bool = True) -> Optional[str]:
        with open(save_path, "rb") as fd: raw = fd.read()
        if len(raw) < 10:
            log.warning(f" - Subtitle file too small ({len(raw)} bytes), skipping conversion")
            return save_path

        stripped_raw = raw.lstrip()
        is_ttml = stripped_raw.startswith(b'<?xml') or stripped_raw.startswith(b'<tt')
        is_vtt = stripped_raw.startswith(b'WEBVTT')
        
        codec = ""
        if is_ttml:
            codec = "ttml"
        elif is_vtt:
            codec = "vtt"
        elif save_path.endswith(".vtt") or save_path.endswith(".webvtt"):
            codec = "vtt"
        elif save_path.endswith(".ttml") or save_path.endswith(".dfxp"):
            codec = "ttml"
        elif save_path.endswith(".ass") or save_path.endswith(".ssa"):
            codec = "ass"
        else:
            codec = "unknown"

        if codec.lower() in ["ass", "ssa"]:
            log.info(f" + ASS/SSA subtitle kept in original format")
            return save_path

        srt_obj = None
        if codec.lower() in ["wvtt", "stpp"]:
            log.info(f" + Extracting text from {codec.upper()} container...")
            extracted = SubtitleProcessor.extract_mdat_text(raw, codec)
            if extracted and len(extracted) > 10:
                try:
                    vtt_content = extracted.decode('utf-8', errors='ignore')
                    srt_obj = WebVTTConverter().from_string(vtt_content)
                except Exception as e:
                    log.warning(f" - Failed to decode extracted content: {e}")

        elif codec.lower() in ["vtt", "webvtt"]:
            try:
                if raw.startswith(b'\x00\x00\x00') or (len(raw) > 4 and raw[:4] == b'mdat'):
                    extracted = SubtitleProcessor.extract_mdat_text(raw, "vtt")
                    vtt_content = extracted.decode('utf-8', errors='ignore')
                else:
                    vtt_content = raw.decode('utf-8', errors='ignore')
                srt_obj = WebVTTConverter().from_string(vtt_content)
            except Exception as e:
                log.warning(f" - VTT conversion failed: {e}")

        elif codec.lower() in ["ttml", "dfxp", "smpte"]:
            try:
                srt_obj = SMPTEConverter().from_bytes(raw)
            except Exception as e:
                log.warning(f" - TTML conversion failed: {e}")

        if srt_obj is not None:
            if len(srt_obj) == 0:
                log.warning(f" - Subtitle parsed but empty, skipping conversion")
                return save_path
            try:
                fixer = CommonIssuesFixer()
                fixer.remove_gaps = True
                srt_obj, _ = fixer.from_srt(srt_obj)
                if strip_sdh:
                    stripper = SDHStripper()
                    srt_obj, status = stripper.from_srt(srt_obj)
                    if status:
                        srt_obj, _ = fixer.from_srt(srt_obj)
                
                srt_path = os.path.splitext(save_path)[0] + '.srt'
                srt_obj.save(Path(srt_path))
                if os.path.exists(save_path) and save_path != srt_path:
                    try: os.unlink(save_path)
                    except: pass
                log.info(f" + Subtitle converted to SRT: {os.path.basename(srt_path)}")
                return srt_path
            except Exception as e:
                log.warning(f" - Post-processing subtitle failed: {e}")
        
        return save_path

    @staticmethod
    def convert_ttml_to_ssa(ttml_data: str, language: str = None) -> str:
        converter = LegacyTTMLConverter(subtitle_language=language)
        converter.parse_ttml_from_string(ttml_data)
        return converter.generate_ssa()

    @staticmethod
    def _extract_wvtt_text_from_mdat(mdat_payload: bytes) -> bytes:
        cues = []
        offset = 0
        while offset + 8 <= len(mdat_payload):
            inner_size = int.from_bytes(mdat_payload[offset:offset + 4], "big")
            inner_type = mdat_payload[offset + 4:offset + 8]
            if inner_size < 8: break

            if inner_type == b"vttc":
                inner_payload = mdat_payload[offset + 8: offset + inner_size]
                cue_data = SubtitleProcessor._parse_vttc_box(inner_payload)
                if cue_data: cues.append(cue_data)
            offset += inner_size

        if not cues: return b""
        return SubtitleProcessor._reconstruct_vtt_from_cues(cues)

    @staticmethod
    def _parse_vttc_box(data: bytes) -> Optional[Dict]:
        result = {"start": None, "end": None, "text": [], "settings": ""}
        offset = 0
        while offset + 8 <= len(data):
            box_size = int.from_bytes(data[offset:offset + 4], "big")
            box_type = data[offset + 4:offset + 8]
            if box_size < 8: break
            payload = data[offset + 8: offset + box_size]

            if box_type == b"payl":
                text = payload.strip(b"\x00").strip()
                if text:
                    try:
                        text_str = text.decode('utf-8', errors='ignore').replace('\x00', '')
                        if text_str.strip(): result["text"].append(text_str)
                    except: pass
            elif box_type == b"sttg":
                try: result["settings"] = payload.decode('utf-8', errors='ignore').strip()
                except: pass
            elif box_type == b"idnt":
                try:
                    ident = payload.decode('utf-8', errors='ignore')
                    if '-->' in ident:
                        parts = ident.split('-->')
                        if len(parts) == 2:
                            result["start"] = parts[0].strip()
                            result["end"] = parts[1].strip()
                except: pass
            offset += box_size
        return result if result["text"] else None

    @staticmethod
    def _reconstruct_vtt_from_cues(cues: List[Dict]) -> bytes:
        vtt_lines = ["WEBVTT", ""]
        for i, cue in enumerate(cues):
            if not cue["start"] or not cue["end"]:
                start_sec = i * 4; end_sec = start_sec + 4
                start = f"{start_sec // 3600:02d}:{(start_sec % 3600) // 60:02d}:{start_sec % 60:02d}.000"
                end = f"{end_sec // 3600:02d}:{(end_sec % 3600) // 60:02d}:{end_sec % 60:02d}.000"
            else:
                start, end = cue["start"], cue["end"]

            timestamp_line = f"{start} --> {end}"
            if cue["settings"]: timestamp_line += f" {cue['settings']}"
            vtt_lines.append(timestamp_line)

            for text in cue["text"]:
                text = re.sub(r'<c[^>]*>', '', text); text = re.sub(r'</c>', '', text)
                text = re.sub(r'<ruby>', '', text); text = re.sub(r'</ruby>', '', text)
                text = re.sub(r'<rt>', '', text); text = re.sub(r'</rt>', '', text)
                text = re.sub(r'<[0-9:]+>', '', text)
                lines = text.split('\n')
                for line in lines:
                    if line.strip(): vtt_lines.append(line.strip())
            vtt_lines.append("")

        return '\n'.join(vtt_lines).encode('utf-8')
```

### `wpgskd\core\tracks\title.py`

```python
import re
import logging
from enum import Enum
from typing import Optional, List, Any, Iterator  
from wpgskd.core.tracks.tracks import Tracks

log = logging.getLogger("Title")

class Title:
    class Types(Enum):
        MOVIE = 1
        TV = 2
        SONG = 3

    def __init__(self, id_: Any, type_: Types, name: Optional[str] = None, year: Optional[int] = None,
                 season: Optional[int] = None, episode: Optional[Any] = None, episode_name: Optional[str] = None,
                 original_lang: Optional[str] = None, source: Optional[str] = None, 
                 service_data: Optional[dict] = None, filename: Optional[str] = None):
        
        self.id = id_
        self.type = type_
        self.name = name or ""
        self.year = year or 0
        self.season = season or 0
        self.episode = episode or 0
        self.episode_name = episode_name
        self.original_lang = original_lang or "en"
        self.source = source
        self.service_data = service_data or {}
        self.tracks = Tracks()
        self.filename = filename or self._generate_filename()
        
        self.manifest_url: Optional[str] = None
        self.dash_manifest_url: Optional[str] = None
        self.cbr_manifest_url: Optional[str] = None
        self.cvbr_manifest_url: Optional[str] = None

    def __eq__(self, other):
        return isinstance(other, Title) and self.id == other.id

    def __str__(self):
        if self.type == Title.Types.MOVIE:
            return f"{self.name} ({self.year})" if self.year else self.name
        elif self.type == Title.Types.TV:
            ep_str = f"E{int(self.episode):02}" if isinstance(self.episode, int) else f"E{self.episode}"
            s_str = f"S{int(self.season):02}" if isinstance(self.season, int) else f"S{self.season}"
            return f"{self.name} {s_str}{ep_str}"
        return self.name

    def _generate_filename(self) -> str:
        if self.type == Title.Types.MOVIE:
            base = self.name
            if self.year: base += f" ({self.year})"
        elif self.type == Title.Types.TV:
            s_str = f"S{int(self.season):02}" if isinstance(self.season, int) else f"S{self.season}"
            base = f"{self.name} {s_str}"
        else:
            base = self.name
            
        base = re.sub(r'[\\/:*?"<>|]', "", base)
        return base.replace(" ", ".")

    def parse_filename(self, media_info=None, folder: bool = False) -> str:
        from wpgskd.core.utilities import sanitize_filename
        from wpgskd.config import config

        if folder and self.type == Title.Types.TV:
            s_str = f"S{int(self.season):02}" if isinstance(self.season, int) else f"S{self.season}"
            return sanitize_filename(f"{self.name} {s_str}")

        template_str = None
        if hasattr(config, 'output_template'):
            ot = config.output_template
            if isinstance(ot, dict):
                template_str = ot.get('movies') if self.type == Title.Types.MOVIE else ot.get('series')
            elif hasattr(ot, 'movies'):
                template_str = ot.movies if self.type == Title.Types.MOVIE else ot.series

        if not template_str:
            # Fallback if config not loaded properly
            if self.type == Title.Types.MOVIE:
                base = self.name
                if self.year: base += f" ({self.year})"
            elif self.type == Title.Types.TV:
                s_str = f"S{int(self.season):02}" if isinstance(self.season, int) else f"S{self.season}"
                e_str = f"E{int(self.episode):02}" if isinstance(self.episode, int) else f"E{self.episode}"
                base = f"{self.name}.{s_str}{e_str}"
            else:
                base = self.name
            return sanitize_filename(base.replace(" ", "."))

        s_str = e_str = season_episode = ""
        if self.type == Title.Types.TV:
            s_str = f"S{int(self.season):02}" if isinstance(self.season, int) else f"S{self.season}"
            e_str = f"E{int(self.episode):02}" if isinstance(self.episode, int) else f"E{self.episode}"
            season_episode = f"{s_str}{e_str}"

        quality = ""
        v_codec = ""
        a_codec = ""
        
        if hasattr(self, 'tracks') and self.tracks:
            if self.tracks.videos:
                v = self.tracks.videos[0]
                quality = f"{v.height}p" if v.height else ""
                v_codec = v.get_codec_display().replace("H.", "H").replace(" ", "")
            if self.tracks.audios:
                a = self.tracks.audios[0]
                a_codec = a.get_codec_display().replace(" ", "").replace("DD+", "DDP")
                if getattr(a, 'atmos', False) and "Atmos" not in a_codec:
                    a_codec += "Atmos"

        tag = getattr(config, 'tag', '') or ""
        
        replacements = {
            "{title}": self.name or "Unknown",
            "{year}": str(self.year) if self.year else "",
            "{season_episode}": season_episode,
            "{episode_name}": self.episode_name or "",
            "{quality}": quality,
            "{source}": self.source or "",
            "{audio}": a_codec,
            "{video}": v_codec,
            "{tag}": tag
        }

        base = template_str
        for k, v in replacements.items():
            base = base.replace(k, v)

        base = re.sub(r'\.+', '.', base)
        base = base.replace(".-", "-")
        if base.endswith("-"): base = base[:-1]
        base = base.strip(". ")

        return sanitize_filename(base)


class Titles(list):
    def __init__(self, *args, **kwargs):
        items = args[0] if args else []
        if items and not isinstance(items, (list, tuple, set)):
            items = [items]
        super().__init__(items, **kwargs)
        self.title_name = self[0].name if self else None

    def order(self):
        self.sort(key=lambda t: int(getattr(t, 'year', 0) or 0))
        self.sort(key=lambda t: getattr(t, 'episode', 0) or 0)
        self.sort(key=lambda t: int(getattr(t, 'season', 0) or 0))
        return self

    def with_wanted(self, wanted: Optional[List[str]]) -> Iterator[Title]:
        for title in self:
            if not wanted or (title.type == Title.Types.TV and f"{title.season}x{title.episode}" in wanted):
                yield title

    def print(self):
        if any(x.type == Title.Types.TV for x in self):
            season_counts = {}
            for x in self:
                s = getattr(x, 'season', 0)
                season_counts[s] = season_counts.get(s, 0) + 1
            info = ", ".join(f"S{s} ({c} eps)" for s, c in sorted(season_counts.items()))
            log.info(f"Title: {self.title_name} | By Season: {info}")
        else:
            log.info(f"Title: {self.title_name}")
```

### `wpgskd\core\tracks\tracks.py`

```python
import logging
import os
import re 
from enum import Enum
from typing import Optional, List, Any, Iterator
from langcodes import Language

from wpgskd.core.utilities import is_close_match, get_closest_match

log = logging.getLogger("Tracks")

class Track:
    class Descriptor(Enum):
        URL = 1
        M3U = 2
        MPD = 3
        ISM = 4
        DASH = 5
        HLS = 6

    def __init__(self, id_: str, source: str, url: Any, codec: str, language: Any = None, 
                 descriptor: Descriptor = Descriptor.URL, encrypted: bool = False, 
                 pssh: Any = None, pr_pssh: Any = None, kid: str = None, key: str = None, 
                 needs_proxy: bool = False, needs_repack: bool = False, 
                 encryption_scheme: Any = None, **kwargs):
        
        self.id = id_
        self.source = source
        self.url = url
        self.codec = codec
        self.language = Language.get(language or "und")
        self.descriptor = descriptor
        self.encrypted = encrypted
        self.encryption_scheme = encryption_scheme
        self.pssh = pssh
        self.pr_pssh = pr_pssh
        self.kid = kid
        self.key = key
        self.needs_proxy = needs_proxy
        self.needs_repack = needs_repack
        self.duration = kwargs.get("duration")
        self.size = kwargs.get("size")
        
        self.is_original_lang = False
        self._location: Optional[str] = None
        self.extra = kwargs.get("extra", {})

    def __repr__(self):
        return f"{self.__class__.__name__}(id={self.id}, lang={self.language}, codec={self.codec})"

    def __eq__(self, other):
        return isinstance(other, Track) and self.id == other.id

    def get_track_name(self) -> Optional[str]:
        if self.language is None:
            return None
        return None 

    def locate(self) -> Optional[str]:
        return self._location

    def swap(self, target_path: str) -> bool:
        if not os.path.exists(target_path) or not self._location:
            return False
        try:
            os.unlink(self._location)
            os.rename(target_path, self._location)
            return True
        except Exception:
            return False

    def move(self, target_path: str) -> bool:
        src = self.locate()
        if not src or not os.path.exists(src):
            return False
        try:
            import shutil
            os.makedirs(os.path.dirname(target_path), exist_ok=True)
            shutil.move(src, target_path)
            self._location = target_path
            return True
        except Exception:
            return False

    def delete(self):
        if self._location and os.path.exists(self._location):
            try:
                os.unlink(self._location)
            except Exception:
                pass
        self._location = None

    def get_pssh(self, session=None) -> bool:
        if self.descriptor == self.Descriptor.M3U and not getattr(self, '_sub_m3u8_parsed', False):
            self._sub_m3u8_parsed = True
            from wpgskd.core.manifests.m3u8 import parse_media_playlist
            
            data = parse_media_playlist(self.url, session)
            
            wv_pssh = data.get("pssh")
            pr_pssh = data.get("pr_pssh")
            kid = data.get("kid")
            
            if (not wv_pssh and not pr_pssh) and data.get("init_url"):
                try:
                    from wpgskd.core.manifests.map_init import extract_pssh_and_kid
                    if not session:
                        session = requests.Session()
                    resp = session.get(data["init_url"], stream=True)
                    chunk = next(resp.iter_content(20000), b"")
                    pssh_list, kid_hex = extract_pssh_and_kid(chunk)
                    if pssh_list:
                        wv_pssh = pssh_list[0]
                    if kid_hex:
                        kid = kid_hex
                except Exception:
                    pass

            if wv_pssh:
                self.pssh = wv_pssh
            if pr_pssh:
                self.pr_pssh = pr_pssh
            if kid and not self.kid:
                self.kid = kid
                
            if not wv_pssh and not pr_pssh and not data.get("aes_key_uri"):
                self.encrypted = False
                self.encryption_scheme = None
                return False
                
            if not self.pssh and isinstance(self.extra, dict) and self.extra.get("master_pssh"):
                self.pssh = self.extra["master_pssh"]
            if not self.pr_pssh and isinstance(self.extra, dict) and self.extra.get("master_pr_pssh"):
                self.pr_pssh = self.extra["master_pr_pssh"]
                
        return bool(self.pssh or self.pr_pssh)
        
    def get_kid(self, session=None) -> bool:
        if self.kid:
            return True
        return bool(self.kid)

    @staticmethod
    def pt_to_sec(d):
        if isinstance(d, (int, float)):
            return float(d)
        if not d:
            return None
        if d[0:2] == "P0":
            d = d.replace("P0Y0M0DT", "PT")
        if d[0:2] != "PT":
            raise ValueError("Input data is not a valid time string.")
        d = d[2:].upper()
        m = re.findall(r"([\d.]+.)", d)
        return sum(
            float(x[0:-1]) * {"H": 60 * 60, "M": 60, "S": 1}[x[-1].upper()]
            for x in m
        )

    def duration_seconds(self):
        cand = getattr(self, "duration", None)
        if cand is None:
            return None
        if isinstance(cand, (int, float)):
            return float(cand)
        try:
            return float(cand)
        except Exception:
            pass
        try:
            return self.pt_to_sec(str(cand))
        except Exception:
            return None

    def computed_size_bytes(self):
        try:
            bitrate = getattr(self, 'bitrate', None)
            if not bitrate:
                return None
            dur = self.duration_seconds()
            if not dur or dur <= 0:
                return None
            return int((float(bitrate) * float(dur)) / 8.0)
        except Exception:
            return None

    @staticmethod
    def format_hms(seconds):
        if seconds is None:
            return None
        try:
            s = int(round(float(seconds)))
        except Exception:
            return None
        h, rem = divmod(s, 3600)
        m, s = divmod(rem, 60)
        return f"{h:02}h{m:02}m{s:02}s"

    @staticmethod
    def format_size_compact(num_bytes):
        try:
            size = float(num_bytes)
        except Exception:
            return ""
        units = ["B", "KB", "MB", "GB", "TB"]
        i = 0
        while size >= 1024 and i < len(units) - 1:
            size /= 1024.0
            i += 1
        return f"{size:.2f} {units[i]}"

class TextTrack(Track):
    def __init__(self, *args, cc: bool = False, sdh: bool = False, forced: bool = False, **kwargs):
        super().__init__(*args, **kwargs)
        self.cc = cc
        self.sdh = sdh
        self.forced = forced

    def get_track_name(self) -> Optional[str]:
        name = super().get_track_name() or ""
        flag = "CC" if self.cc else "SDH" if self.sdh else "Forced" if self.forced else ""
        if flag:
            name += f" ({flag})" if name else flag
        return name or None

    def __str__(self):
        parts = ["├─ SUB", self.codec or "vtt", str(self.language)]
        flags = []
        if getattr(self, 'is_original_lang', False): flags.append("orig")
        if self.forced: flags.append("Forced")
        if self.sdh: flags.append("SDH")
        if self.cc: flags.append("CC")
        if flags:
            parts.append(" ".join(flags))
        return " | ".join(parts)

    def convert_to_srt(self, strip_sdh: bool = True) -> Optional[str]:
        from wpgskd.core.tracks.subtitles import SubtitleProcessor
        if not self._location:
            log.warning("Cannot convert subtitle, track not downloaded yet.")
            return None
            
        if self.sdh and strip_sdh is None:
            strip_sdh = True
            
        new_path = SubtitleProcessor.convert_subtitle_to_srt(self._location, strip_sdh)
        if new_path and new_path != self._location:
            self._location = new_path
            self.codec = "srt"
        return self._location

class Tracks:
    def __init__(self, *tracks: Track):
        self.videos: List[Any] = []  # VideoTrack
        self.audios: List[Any] = []  # AudioTrack
        self.subtitles: List[TextTrack] = []
        self.chapters: List[Any] = []

        if tracks:
            self.add(list(tracks))

    def __iter__(self) -> Iterator[Track]:
        return iter(self.videos + self.audios + self.subtitles)

    def add(self, tracks: Any, warn_only: bool = True):
        if tracks is None:
            return
            
        if isinstance(tracks, Tracks):
            tracks = list(tracks) + tracks.chapters
        elif isinstance(tracks, Track):
            tracks = [tracks]
            
        existing_ids = {t.id for t in self}
        
        for track in tracks:
            if track.id in existing_ids:
                if not warn_only:
                    raise ValueError(f"Duplicate Track ID: {track.id}")
                continue
            
            existing_ids.add(track.id)
            
            cls_name = track.__class__.__name__
            if cls_name == "VideoTrack":
                self.videos.append(track)
            elif cls_name == "AudioTrack":
                self.audios.append(track)
            elif cls_name == "TextTrack":
                self.subtitles.append(track)
            elif cls_name == "MenuTrack":
                self.chapters.append(track)

    def sort_videos(self, by_language: Optional[List[str]] = None):
        if not self.videos: return
        def range_priority(x):
            if getattr(x, 'dv', False): return 4
            if getattr(x, 'hdr10', False) or getattr(x, 'dvhdr', False): return 3
            if getattr(x, 'hlg', False): return 1
            return 2 # SDR
        self.videos.sort(key=lambda x: (range_priority(x), float(x.bitrate or 0.0)), reverse=True)

    def sort_audios(self, by_language: Optional[List[str]] = None):
        if not self.audios: return
        self.audios.sort(key=lambda x: float(x.bitrate or 0.0), reverse=True)
        self.audios.sort(key=lambda x: "" if x.descriptive else str(x.language))

        if by_language:
            for lang in reversed(by_language):
                if str(lang) == "all":
                    lang = next((x.language for x in self.audios if x.is_original_lang), "")
                if not lang: continue
                self.audios.sort(key=lambda x: "" if is_close_match(lang, [x.language]) else str(x.language))
                
    def sort_subtitles(self, by_language: Optional[List[str]] = None):
        if not self.subtitles: return
        self.subtitles.sort(key=lambda x: str(x.language) + ("-cc" if x.cc else "") + ("-sdh" if x.sdh else ""))
        self.subtitles.sort(key=lambda x: not x.forced)
        if by_language:
            for lang in reversed(by_language):
                if str(lang) == "all":
                    lang = next((x.language for x in self.subtitles if x.is_original_lang), "")
                if not lang: continue
                self.subtitles.sort(key=lambda x: "" if is_close_match(lang, [x.language]) else str(x.language))

    def sort_chapters(self):
        if not self.chapters: return
        self.chapters.sort(key=lambda x: x.number)

    def select_videos(self, by_quality=None, by_vbitrate=None, by_range=None, one_only=True, by_worst=False, by_codec=None):
        videos = self.videos
        if by_quality:
            q_videos = [x for x in videos if x.height == by_quality]
            if not q_videos: q_videos = [x for x in videos if int(x.width * (9/16)) == by_quality]
            if not q_videos and by_quality == "SD": q_videos = [x for x in videos if (x.width, x.height) < (1024, 576)]
            if not q_videos and by_quality == "HD720": q_videos = [x for x in videos if (x.width, x.height) < (1482, 620)]
            if not q_videos: raise ValueError(f"No {by_quality}p video track.")
            videos = q_videos
            
        if by_vbitrate:
            videos = [x for x in videos if int(x.bitrate or 0) <= int(by_vbitrate * 1001)]
        if by_worst:
            videos.sort(key=lambda x: float(x.bitrate or 0.0))
        if by_codec:
            target = by_codec.upper()
            c_videos = []
            for x in videos:
                raw = (x.codec or "").lower()
                if any(k in raw for k in ["hev", "hvc", "dvh"]):
                    std = "H265"
                elif "avc" in raw:
                    std = "H264"
                elif "av01" in raw or "dav1" in raw:
                    std = "AV1"
                elif "vp09" in raw or raw == "vp9":
                    std = "VP9"
                else:
                    std = raw.upper()
                if std == target: c_videos.append(x)
            if not c_videos: raise ValueError(f"No {by_codec} video tracks.")
            videos = c_videos
        if by_range:
            target_range = by_range.upper()
            if target_range == "DV+HDR":
                videos = [x for x in videos if getattr(x, 'dv', False) and getattr(x, 'hdr10', False)]
            elif target_range == "DV":
                videos = [x for x in videos if getattr(x, 'dv', False)]
            elif target_range == "HDR10":
                videos = [x for x in videos if getattr(x, 'hdr10', False) and not getattr(x, 'dv', False)]
            elif target_range == "HLG":
                videos = [x for x in videos if getattr(x, 'hlg', False)]
            elif target_range == "SDR":
                videos = [x for x in videos if not x.hdr10 and not x.dv and not x.hlg and not getattr(x, 'dvhdr', False)]
            else:
                raise ValueError(f"Unsupported range: {by_range}")
                
            if not videos: raise ValueError(f"No {by_range} video track.")
            
        if one_only and videos:
            self.videos = [videos[0]]
        else:
            self.videos = videos

    def select_videos_multi(self, ranges: list[str], by_quality=None, by_vbitrate=None, by_worst=False):
        videos = self.videos
        
        for r in ranges:
            r_upper = r.upper()
            if r_upper == "DV":
                videos = [x for x in videos if getattr(x, 'dv', False)]
            elif r_upper == "HDR10":
                videos = [x for x in videos if getattr(x, 'hdr10', False)]
            elif r_upper == "HLG":
                videos = [x for x in videos if getattr(x, 'hlg', False)]
            elif r_upper == "DVHDR": 
                videos = [x for x in videos if getattr(x, 'dvhdr', False)]

        if not videos:
            raise ValueError(f"No video tracks matching all ranges: {ranges}")

        if by_quality:
            q_videos = [x for x in videos if x.height == by_quality]
            if not q_videos: q_videos = [x for x in videos if int(x.width * (9/16)) == by_quality]
            if not q_videos and by_quality == "SD": q_videos = [x for x in videos if (x.width, x.height) < (1024, 576)]
            if not q_videos and by_quality == "HD720": q_videos = [x for x in videos if (x.width, x.height) < (1482, 620)]
            if not q_videos: raise ValueError(f"No {by_quality}p video track in {ranges}.")
            videos = q_videos

        if by_vbitrate:
            videos = [x for x in videos if int(x.bitrate or 0) <= int(by_vbitrate * 1001)]

        if by_worst:
            videos.sort(key=lambda x: float(x.bitrate or 0.0))
        else:
            videos.sort(key=lambda x: float(x.bitrate or 0.0), reverse=True)

        if videos:
            self.videos = [videos[0]]
        else:
            self.videos = videos

    def select_audios(self, by_language=None, by_bitrate=None, with_atmos=False, with_descriptive=True, by_channels=None, by_codec=None):
        audios = self.audios
        
        if not with_descriptive:
            audios = [x for x in audios if not x.descriptive]
           
        if by_codec:
            target = by_codec.upper()
            c_audios = []
            for x in audios:
                raw = (x.codec or "").lower()
                std = "EC3" if any(k in raw for k in ["ec-3", "eac3"]) else "AC3" if "ac-3" in raw else "AAC" if "aac" in raw else raw.upper()
                if std == target: c_audios.append(x)
            if c_audios: audios = c_audios
            
        if with_atmos:
            atmos = [x for x in audios if x.atmos]
            if atmos: audios = atmos
            
        if by_channels:
            ch_audios = [x for x in audios if x.channels == by_channels]
            if ch_audios: audios = ch_audios
           
        if by_bitrate:
            audios = [x for x in audios if int(x.bitrate or 0) <= int(by_bitrate * 1000)]
            
        if by_language:
            if "all" in by_language:
                pass #
            else:
                filtered_audios = []
                orig_lang_audios = [x for x in audios if x.is_original_lang]
                
                for x in audios:
                    lang_str = str(x.language).lower()
                    base_lang = lang_str.split("-")[0]
                    
                    is_match = False
                    for req_lang in by_language:
                        req_lang_str = str(req_lang).lower()
                        
                        if req_lang_str == "orig":
                            if x in orig_lang_audios:
                                is_match = True
                                break
                        elif lang_str == req_lang_str:
                            is_match = True
                            break
                        elif "-" not in req_lang_str and base_lang == req_lang_str:
                            is_match = True
                            break
                            
                    if is_match:
                        filtered_audios.append(x)
                        
                audios = filtered_audios
                
            best_tracks = {}
            requested_langs_lower = [str(l).lower() for l in by_language]
            
            for x in audios:
                lang_str = str(x.language).lower()
                base_lang = lang_str.split("-")[0]
                
                key = lang_str
                if lang_str not in requested_langs_lower:
                    for req_lang in by_language:
                        req_lang_str = str(req_lang).lower()
                        if "-" not in req_lang_str and base_lang == req_lang_str:
                            key = req_lang_str
                            break
                            
                bitrate = float(x.bitrate or 0.0)
                if key not in best_tracks or bitrate > best_tracks[key][1]:
                    best_tracks[key] = (x, bitrate)
                    
            audios = list(best_tracks.values())
            audios = [v[0] for v in audios]
            
        self.audios = audios
                      
    def select_subtitles(self, by_language=None, with_forced=None):
        subs = self.subtitles
        if by_language:
            filtered = []
            for lang in by_language:
                if str(lang) == "all":
                    filtered.extend(subs)
                elif str(lang) == "orig":
                    filtered.extend([x for x in subs if x.is_original_lang])
                else:
                    match = get_closest_match(lang, [x.language for x in subs])
                    if match:
                        filtered.extend([x for x in subs if x.language == match])
            
            seen_ids = set()
            deduped = []
            for x in filtered:
                if x.id not in seen_ids:
                    seen_ids.add(x.id)
                    deduped.append(x)
            subs = deduped
            
        if with_forced is False:
            subs = [x for x in subs if not x.forced]
            
        self.subtitles = subs           
    
    @staticmethod
    def from_mpd(*args, **kwargs):
        from wpgskd.core.manifests.dash import parse as parse_mpd
        return parse_mpd(*args, **kwargs)

    @staticmethod
    def from_m3u8(*args, **kwargs):
        from wpgskd.core.manifests.hls import parse as parse_hls
        return parse_hls(*args, **kwargs)

    @staticmethod
    def from_ism(*args, **kwargs):
        from wpgskd.core.manifests.ism import parse as parse_ism
        return parse_ism(*args, **kwargs)        
```

### `wpgskd\core\tracks\video.py`

```python
import math
from typing import Optional
from wpgskd.core.tracks.tracks import Track

VIDEO_CODEC_MAP = {
    "AVC": "H.264",
    "HEVC": "H.265",
    "V_VC1": "VC-1",
    "V_MPEGH/ISO/HEVC": "H.265",
    "V_MPEG4/ISO/AVC": "H.264",
    "AV1": "AV1",
    "VP8": "VP8",
    "VP9": "VP9",
}

class VideoTrack(Track):
    def __init__(self, *args, bitrate: int, width: int, height: int, fps: Optional[float] = None,
                 hdr10: bool = False, dvhdr: bool = False, hlg: bool = False, dv: bool = False, 
                 needs_ccextractor: bool = False, mpd_representation_id: Optional[str] = None, **kwargs):
        super().__init__(*args, **kwargs)
        self.bitrate = int(math.ceil(float(bitrate))) if bitrate else None
        self.width = int(width)
        self.height = int(height)
        self.fps = float(fps) if fps else None
        
        self.hdr10 = bool(hdr10)
        self.dvhdr = bool(dvhdr)
        self.hlg = bool(hlg)
        self.dv = bool(dv)
        
        self.needs_ccextractor = needs_ccextractor
        self.mpd_representation_id = mpd_representation_id

    def get_codec_display(self) -> str:
        if not self.codec:
            return "Unknown"
            
        codec_str = str(self.codec)
        codec_lower = codec_str.lower()
        
        if codec_str in VIDEO_CODEC_MAP:
            return VIDEO_CODEC_MAP[codec_str]
            
        if "avc" in codec_lower or "h264" in codec_lower:
            return "H.264"
        elif "hev" in codec_lower or "hvc" in codec_lower or "h265" in codec_lower or "dvh" in codec_lower:
            return "H.265"
        elif "av1" in codec_lower:
            return "AV1"
        elif "vp09" in codec_lower or "vp9" in codec_lower:
            return "VP9"
        elif "vp08" in codec_lower or "vp8" in codec_lower:
            return "VP8"
        elif "vc-1" in codec_lower or "vc1" in codec_lower:
            return "VC-1"           
        return codec_str

    def __str__(self):
        codec = self.get_codec_display()
        range_str = "DV+HDR" if self.dvhdr else "HDR10" if self.hdr10 else "HLG" if self.hlg else "DV" if self.dv else "SDR"
        fps_str = f"{self.fps:.3f} FPS" if self.fps else "Unknown FPS"
        bitrate_str = f"{self.bitrate // 1000 if self.bitrate else '?'} kb/s"
        enc_str = "Encrypted" if self.encrypted else "Unencrypted"
        
        dur_sec = self.duration_seconds()
        size_bytes = self.size if self.size else self.computed_size_bytes()
        size_str = self.format_size_compact(size_bytes) if size_bytes else None
        dur_str = self.format_hms(dur_sec) if dur_sec else None

        return " | ".join([x for x in [
            "├─ VID",
            codec,
            range_str,
            f"{self.width}x{self.height}",
            bitrate_str,
            fps_str,
            enc_str,
            size_str,
            dur_str
        ] if x])
```

### `wpgskd\servicookies\BaseService.py`

```python
import json
import logging
import os
import sys
import re
import yaml
from abc import ABC, abstractmethod
from http.cookiejar import MozillaCookieJar

import requests
from requests.adapters import HTTPAdapter, Retry
import random

from wpgskd import config as config_module 
from wpgskd.utils import try_get
from wpgskd.utils.collections import as_list, merge_dict
from wpgskd.utils.io import get_ip_info


class BaseService(ABC):
    ALIASES = []  
    GEOFENCE = []  

    def __init__(self, ctx):
        self.service_path = sys.modules[self.__module__].__file__
        self.service_dir = os.path.dirname(self.service_path)
        self.service_name = self.__class__.__name__

        self.log = logging.getLogger(self.ALIASES[0])
        
        self.service_config = self.load_local_config()
        self.local_cookies = self.load_local_cookies()

        self.config = ctx.obj.config if hasattr(ctx.obj, 'config') else {}
        
        if self.service_config:
            merge_dict(self.config, self.service_config)

        self.cookies = ctx.obj.cookies if hasattr(ctx.obj, 'cookies') else None
        self.credentials = ctx.obj.credentials if hasattr(ctx.obj, 'credentials') else None
        
        self.cdm = ctx.obj.cdm if hasattr(ctx.obj, 'cdm') else None
        self.vaults = ctx.obj.vaults if hasattr(ctx.obj, 'vaults') else None
        self.profile = ctx.obj.profile if hasattr(ctx.obj, 'profile') else None

        self.session = self.get_session()
        self.force_proxy = ctx.parent.params.get("force_proxy", False)

        if not ctx.parent.params.get("no_proxy"):
            self.setup_proxy(ctx)

    def get_session(self):
        session = requests.Session()
        session.mount("https://", HTTPAdapter(
            max_retries=Retry(
                total=5,
                backoff_factor=1,
                status_forcelist=[429, 500, 502, 503, 504],
            )
        ))
        session.hooks = {
            "response": lambda r, *_, **__: r.raise_for_status(),
        }
        
        if hasattr(config_module, 'config') and hasattr(config_module.config, 'headers'):
            headers = config_module.config.headers
            if isinstance(headers, dict):
                session.headers.update(headers)
        
        if self.local_cookies:
            session.cookies.update(self.local_cookies)
        elif self.cookies:
            session.cookies.update(self.cookies)
            
        return session

    def load_local_config(self):
        candidates = [
            os.path.join(self.service_dir, f"{self.service_name}.yml"),
            os.path.join(self.service_dir, f"{self.service_name.lower()}.yml")
        ]
        for path in candidates:
            if os.path.exists(path):
                self.log.debug(f"Loading local config: {path}")
                try:
                    with open(path, 'r', encoding='utf-8') as f:
                        return yaml.safe_load(f) or {}
                except Exception as e:
                    self.log.warning(f"Failed to load config {path}: {e}")
        return {}

    def load_local_cookies(self):
        cookie_path = os.path.join(self.service_dir, "cookie.txt")
        if os.path.exists(cookie_path):
            self.log.debug(f"Loading local cookies: {cookie_path}")
            try:
                cj = MozillaCookieJar(cookie_path)
                cj.load(ignore_discard=True, ignore_expires=True)
                return cj
            except Exception as e:
                self.log.warning(f"Failed to load cookies {cookie_path}: {e}")
        return None

    def setup_proxy(self, ctx):
        proxy = ctx.parent.params.get("proxy") or next(iter(self.GEOFENCE), None)
        if proxy:
            if len("".join(i for i in proxy if not i.isdigit())) == 2:
                proxy = self.get_proxy(proxy)
            if proxy:
                if "://" not in proxy: proxy = f"https://{proxy}"
                self.session.proxies.update({"all": proxy})
                self.log.info(f"Using Proxy: {proxy}")
            else:
                self.log.info(" + Proxy was skipped as current region matches")

    @abstractmethod
    def get_titles(self):
        raise NotImplementedError

    @abstractmethod
    def get_tracks(self, title):
        raise NotImplementedError

    def get_chapters(self, title):
        return []

    def certificate(self, challenge, title, track, session_id):
        return self.license(challenge, title, track, session_id)

    @abstractmethod
    def license(self, challenge, title, track, session_id, drm_type=None):
        raise NotImplementedError

    def parse_title(self, ctx, title):
        title = title or ctx.parent.params.get("title")
        if not title:
            self.log.exit(" - No title ID specified")
        if not getattr(self, "TITLE_RE", None):
            self.title = title
            return {}
        for regex in as_list(self.TITLE_RE):
            m = re.search(regex, title)
            if m:
                self.title = m.group("id")
                return m.groupdict()
        self.log.warning(f" - Unable to parse title ID {title!r}, using as-is")
        self.title = title

    def get_cache(self, key):
        from wpgskd.config import directories
        cache_dir = getattr(directories, 'cache', None)
        if not cache_dir:
            cache_dir = os.path.join(os.getcwd(), "cache")
        target_dir = os.path.join(cache_dir, self.ALIASES[0])
        os.makedirs(target_dir, exist_ok=True)
        return os.path.join(target_dir, key)

    def get_proxy(self, region):
        if not region:
            raise self.log.exit("Region cannot be empty")
        region = region.lower()

        self.log.info(f"Obtaining a proxy to \"{region}\"")

        if not self.force_proxy and get_ip_info()["country_code"].lower() == "".join(char for char in region if not char.isdigit()):
            return None

        if getattr(config_module.config, 'proxies', {}).get(region) and not getattr(config_module.config, 'default_proxy_service', None):
            proxy = config_module.config.proxies[region]
            self.log.info(f" + {proxy}")
        else:
            default_service = getattr(config_module.config, 'default_proxy_service', None)
            proxy = None

            if default_service == "nordvpn" and getattr(config_module.config, 'nordvpn', {}).get("username") and getattr(config_module.config, 'nordvpn', {}).get("password"):
                proxy = self.get_nordvpn_proxy(region)
                self.log.info(f" + {proxy} (via NordVPN)")
            elif default_service == "surfshark" and getattr(config_module.config, 'surfshark', {}).get("username") and getattr(config_module.config, 'surfshark', {}).get("password"):
                proxy = self.get_surfshark_proxy(region, config_module.config.surfshark)
                self.log.info(f" + {proxy} (via SurfShark)")
            else:
                raise self.log.exit(" - Unable to obtain a proxy")

        if "://" not in proxy:
            proxy = f"https://{proxy}"

        return proxy

    def get_nordvpn_proxy(self, region):
        proxy = f"https://{config_module.config.nordvpn['username']}:{config_module.config.nordvpn['password']}@"
        if any(char.isdigit() for char in region):
            proxy += f"{region}.nordvpn.com"
        elif try_get(config_module.config.nordvpn, lambda x: x["servers"][region]):
            proxy += f"{region}{config_module.config.nordvpn['servers'][region]}.nordvpn.com"
        else:
            hostname = self.get_nordvpn_server(region)
            if not hostname:
                raise self.log.exit(f" - NordVPN doesn't contain any servers for the country \"{region}\"")
            proxy += hostname
        return proxy + ":89"

    def get_nordvpn_server(self, country):
        countries = self.session.get(
            url="https://api.nordvpn.com/v1/servers/countries"
        ).json()

        country_id = [x["id"] for x in countries if x["code"].lower() == country.lower()]
        if not country_id:
            return None
        country_id = country_id[0]

        recommendations = self.session.get(
            url="https://api.nordvpn.com/v1/servers/recommendations",
            params={
                "filters[country_id]": country_id,
                "limit": 30
            }
        ).json()
        hostnames = [host["hostname"] for host in recommendations]
        chosen_host = random.choice(hostnames)

        return chosen_host

    def get_surfshark_proxy(self, region, data):
        proxy = f"https://{data['username']}:{data['password']}@"
        if not (hostname := self.get_surfshark_server(region)):
            raise ValueError(
                f"SurfShark doesn't contain any servers for the country {region!r}"
            )
        proxy += hostname
        return proxy + ":443"

    def get_surfshark_server(self, country):
        response = self.session.get(
            url='https://api.surfshark.com/v5/server/clusters/all'
        )
        countries = response.json()

        if not (
            items := [
                x
                for x in countries
                if x["countryCode"].lower() == country.lower()
                and x["type"].lower() not in ("obfuscated", "static")
            ]
        ):
            return None

        hostname = min(items, key=lambda x: x["load"])["connectionName"]

        return hostname
```

### `wpgskd\servicookies\__init__.py`

```python
import os
import logging
import importlib.util
import sys
import traceback
from wpgskd.servicookies.BaseService import BaseService

SERVICE_MAP = {}
log = logging.getLogger("ServiceLoader")

BASE_DIR = os.path.dirname(os.path.abspath(__file__))

def load_services():
    """
    Dynamically load all service modules.
    """
    count = 0

    for item in os.listdir(BASE_DIR):
        item_path = os.path.join(BASE_DIR, item)
        
        if os.path.isdir(item_path) and not item.startswith("_") and item != "dm":
            
            candidates = []
            exact_match = os.path.join(item_path, f"{item.lower()}.py")
            if os.path.exists(exact_match):
                candidates.append(exact_match)
            else:
                for f in os.listdir(item_path):
                    if f.endswith(".py") and not f.startswith("__") and not f.endswith("_pb2.py"):
                        candidates.append(os.path.join(item_path, f))
            
            for py_file in candidates:
                try:
                    module_name = f"wpgskd.servicookies.{item}.{os.path.splitext(os.path.basename(py_file))[0]}"
                    
                    spec = importlib.util.spec_from_file_location(module_name, py_file)
                    if spec and spec.loader:
                        module = importlib.util.module_from_spec(spec)
                        sys.modules[module_name] = module
                        spec.loader.exec_module(module)
                        
                        for name, obj in module.__dict__.items():
                            if isinstance(obj, type) and issubclass(obj, BaseService) and obj != BaseService:
                                SERVICE_MAP[name] = obj.ALIASES
                                globals()[name] = obj
                                count += 1
                                # log.info(f"Loaded service: {name}")
                except Exception as e:
                    print(f"\n[ERROR] Failed to load service from {py_file}")
                    print(f"Reason: {e}")
                    traceback.print_exc()
                    print("-" * 30 + "\n")

    log.info(f"Loaded {count} services.")

load_services()

import os
import html
from http.cookiejar import MozillaCookieJar
from wpgskd.config import filenames, directories
from wpgskd.utils.io import load_yaml
from wpgskd.utils.collections import merge_dict
from wpgskd.core.credential import Credential

def get_service_config(service: str) -> dict:
    """Get both service config and service secrets as one merged dictionary."""
    service_config = load_yaml(filenames.service_config.format(service=service.lower()))

    user_config_path = os.path.join(directories.service_configs, f"{service.lower()}.yml")
    if os.path.exists(user_config_path):
        user_config = load_yaml(user_config_path)
        if user_config:
            merge_dict(service_config, user_config)
            
    return service_config

def get_cookie_jar(service: str, profile: str):
    """Get the profile's cookies if available."""
    cookie_file = os.path.join(directories.cookies, service.lower(), f"{profile}.txt")
    if not os.path.isfile(cookie_file):
        cookie_file = os.path.join(directories.cookies, service.lower(), "default.txt")
        
    if os.path.isfile(cookie_file):
        cookie_jar = MozillaCookieJar(cookie_file)
        with open(cookie_file, "r+", encoding="utf-8") as fd:
            unescaped = html.unescape(fd.read())
            fd.seek(0)
            fd.truncate()
            fd.write(unescaped)
        cookie_jar.load(ignore_discard=True, ignore_expires=True)
        return cookie_jar
    return None

def get_credentials(service: str, profile: str = "default"):
    """Get the profile's credentials if available."""
    from wpgskd.config import config
    cred = config.credentials.get(service, {})

    if isinstance(cred, dict):
        cred = cred.get(profile)
    elif profile != "default":
        return None

    if cred:
        if isinstance(cred, list):
            return Credential(*cred)
        else:
            return Credential.loads(cred)
    return None

def get_service_key(value):
    value = value.lower()
    for key, aliases in SERVICE_MAP.items():
        if value in map(str.lower, aliases) or value == key.lower():
            return key
    return None
```

### `wpgskd\servicookies\example\default.txt`

```

```

### `wpgskd\servicookies\example\example.py`

```python
from wpgskd.core.tracks import Title, Tracks, AudioTrack, TextTrack, MenuTrack, VideoTrack, Track
from wpgskd.servicookies.BaseService import BaseService
```

### `wpgskd\servicookies\example\example.yml`

```yaml

```

### `wpgskd\utils\gen_esn.py`

```python
from datetime import datetime, timedelta
import os
import logging
import random


log = logging.getLogger("NF-ESN")

def chrome_esn_generator():

    ESN_GEN = "".join(random.choice("0123456789ABCDEF") for _ in range(30))
    esn_file = '.esn'
    
    def gen_file():
        with open(esn_file, 'w') as file:
            file.write(f'NFCDIE-03-{ESN_GEN}')
    
    if not os.path.isfile(esn_file):
        log.warning("Generating a new Chrome ESN")
        gen_file()
    
    file_datetime = datetime.fromtimestamp(os.path.getmtime(esn_file))
    time_diff = datetime.now() - file_datetime
    if time_diff > timedelta(hours=6):
        log.warning("Old ESN detected, Generating a new Chrome ESN")
        gen_file()

    with open(esn_file, 'r') as f:
        esn =  f.read()

    return esn
```

### `wpgskd\utils\MSL\MSLKeys.py`

```python
from wpgskd.utils.MSL.MSLObject import MSLObject


class MSLKeys(MSLObject):
    def __init__(self, encryption=None, sign=None, rsa=None, mastertoken=None, cdm_session=None):
        self.encryption = encryption
        self.sign = sign
        self.rsa = rsa
        self.mastertoken = mastertoken
        self.cdm_session = cdm_session
```

### `wpgskd\utils\MSL\MSLObject.py`

```python
import jsonpickle


class MSLObject:
    def __repr__(self):
        return "<{} {}>".format(self.__class__.__name__, jsonpickle.encode(self, unpicklable=False))
```

### `wpgskd\utils\MSL\MSL_ANDROID.py`

```python
import base64
import gzip
import json
import random
import sys
import zlib
import jsonpickle
import requests
from io import BytesIO
from pathlib import Path
from datetime import datetime, timezone
from typing import Any, Dict, List, Optional, Tuple
from Cryptodome.Cipher import AES
from Cryptodome.Hash import HMAC, SHA256
from Cryptodome.PublicKey.RSA import RsaKey
from Cryptodome.Random import get_random_bytes
from Cryptodome.Util import Padding
from scripts.pywidevine import Cdm as WidevineCdm, Device as WidevineDevice, PSSH

class MSLAndroidObject:
    def __repr__(self) -> str:
        return f"<{self.__class__.__name__} {jsonpickle.encode(self, unpicklable=False)}>"


class MSLAndroidKeys(MSLAndroidObject):
    def __init__(
        self,
        encryption: Optional[bytes] = None,
        sign: Optional[bytes] = None,
        rsa: Optional[RsaKey] = None,
        mastertoken: Optional[dict] = None,
        cdm_session: Any = None,
    ):
        self.encryption = encryption
        self.sign = sign
        self.rsa = rsa
        self.mastertoken = mastertoken
        self.cdm_session = cdm_session

class MSLAndroid:
    DEFAULT_HANDSHAKE_ENDPOINT = "https://android.prod.ftl.netflix.com/nq/androidui/pbo_license/~1.0.0/router"
    DEFAULT_MANIFEST_ENDPOINT = "https://android.prod.ftl.netflix.com/msl/playapi/android/manifest"
    DEFAULT_MANIFEST_PARAMS = {
        "ab_ui_ver": "android",
        "nrdapp_version": "18.26.0",
    }
    DEFAULT_USER_AGENT = "com.netflix.mediaclient/63988 (Linux; U; Android 15; en_US; SM-F711N; Build/AP3A.240905.015.A2; Cronet/143.0.7445.0)"
    DEFAULT_REQUEST_CONTEXT = '{"appState":"foreground","appView":"unknown"}'
    DEFAULT_NRDJS_VERSION = "v3.12.55"
    DEFAULT_NETJS_VERSION = "3.0.5"
    DEFAULT_PBO_VERSION = 2
    DEFAULT_PBO_COMMON = {
        "sdk": "18.26.0",
        "platform": "18.26.0",
        "application": "Netflix Android 18.26.0",
        "uiversion": "18.26.0",
        "uiPlatform": "android",
        "clientVersion": "18.26.0",
        "apkVersion": "18.26.0",
    }
    DEFAULT_PBO_LANGUAGES = ["en-US", "en"]
    DEFAULT_DEVICE_MODEL = "SM-F711N"

    def __init__(
        self,
        session: requests.Session,
        keys: MSLAndroidKeys,
        message_id: int,
        sender: str,
        user_auth: Optional[dict] = None,
        drm: str = "widevine",
    ):
        self.session = session
        self.keys = keys
        self.sender = sender
        self.user_auth = user_auth
        self.message_id = message_id
        self.drm = drm

    @classmethod
    def handshake(
        cls,
        msl_keys_path: str,
        session: requests.Session,
        sender: str,
        cdm: Any,
        cdm_device: Any,
        new_msl: bool,
        cookies: Optional[Dict[str, str]],
        drm: str,
        endpoint: Optional[str] = None,
        headers: Optional[Dict[str, str]] = None,
    ) -> MSLAndroidKeys:
        if cookies:
            session.cookies.update(cookies)

        cache_path = Path(msl_keys_path)
        msl_keys = MSLAndroid.load_cache_data(cache_path)
        if msl_keys is not None and not new_msl:
            return msl_keys

        if drm != "widevine":
            raise ValueError(f"Unsupported DRM mode: {drm}")

        if not cdm:
            raise ValueError("Widevine CDM is required for this iOS MSL flow")

        message_id = random.randint(0, pow(2, 52))
        msl_keys = MSLAndroidKeys()

        if not isinstance(cdm, WidevineCdm):
            device = WidevineDevice.load(cdm_device)
            cdm = WidevineCdm.from_device(device)

        cdm_session = cdm.open()
        msl_keys.cdm_session = cdm_session
        challenge = cdm.get_license_challenge(
            cdm_session,
            PSSH.new(system_id=PSSH.SystemId.Widevine),
        )
        wv_request = base64.b64encode(challenge).decode("utf-8")
        keyrequestdata = {
            "scheme": "WIDEVINE",
            "keydata": {
                "keyrequest": wv_request,
            },
        }

        data = jsonpickle.encode(
            {
                "entityauthdata": {
                    "scheme": "NONE",
                    "authdata": {
                        "identity": sender,
                    },
                },
                "headerdata": base64.standard_b64encode(
                    MSLAndroid.generate_msg_header(
                        message_id=message_id,
                        sender=sender,
                        is_handshake=True,
                        keyrequestdata=keyrequestdata,
                    ).encode("utf-8")
                ).decode("utf-8"),
                "signature": "",
            },
            unpicklable=False,
        )
        data += json.dumps(
            {
                "payload": base64.standard_b64encode(
                    json.dumps(
                        {
                            "messageid": message_id,
                            "data": "",
                            "sequencenumber": 1,
                            "endofmsg": True,
                        }
                    ).encode("utf-8")
                ).decode("utf-8"),
                "signature": "",
            }
        )

        handshake_endpoint = endpoint or cls.DEFAULT_HANDSHAKE_ENDPOINT
        handshake_headers = headers or cls.build_request_headers(
            request_name="mintCookies",
            esn=sender,
            host="android15.prod.cloud.netflix.com",
            language="en-US,en",
        )
        res = session.post(url=handshake_endpoint, data=data, headers=handshake_headers, timeout=30)

        if res.status_code != 200:
            raise RuntimeError(f"Key exchange failed: HTTP {res.status_code} {res.text[:500]}")

        parsed = cls.parse_concatenated_json(res.text)
        if not parsed:
            raise RuntimeError("Key exchange failed: empty MSL response")

        key_exchange = parsed[0]

        if "errordata" in key_exchange:
            decoded_error = base64.standard_b64decode(key_exchange["errordata"]).decode("utf-8")
            error_json = json.loads(decoded_error)
            raise RuntimeError(f"Key exchange failed: {error_json}")

        if "headerdata" not in key_exchange:
            raise RuntimeError(f"Key exchange failed: missing headerdata in response: {str(key_exchange)[:500]}")

        header_json = json.loads(
            base64.standard_b64decode(key_exchange["headerdata"]).decode("utf-8")
        )
        key_response_data = header_json["keyresponsedata"]
        key_data = key_response_data["keydata"]

        cdm.parse_license(msl_keys.cdm_session, key_data["cdmkeyresponse"])
        keys = cdm.get_keys(msl_keys.cdm_session)
        msl_keys.encryption = MSLAndroid.get_widevine_key(
            kid=base64.standard_b64decode(key_data["encryptionkeyid"]),
            keys=keys,
            permissions=["AllowEncrypt", "AllowDecrypt"],
        )
        msl_keys.sign = MSLAndroid.get_widevine_key(
            kid=base64.standard_b64decode(key_data["hmackeyid"]),
            keys=keys,
            permissions=["AllowSign", "AllowSignatureVerify"],
        )

        msl_keys.mastertoken = key_response_data["mastertoken"]
        MSLAndroid.cache_keys(msl_keys, cache_path)
        return msl_keys

    @staticmethod
    def build_request_headers(
        request_name: str,
        user_agent: Optional[str] = None,
        referer: Optional[str] = None,
        viewable_id: Optional[int] = None,
        profile_guid: Optional[str] = None,
        esn: Optional[str] = None,
        expiry_timeout: Optional[int] = 12750,
        extra_headers: Optional[Dict[str, str]] = None,
        host: Optional[str] = "android15.prod.cloud.netflix.com",
        language: Optional[str] = "en-US",
        device_model: Optional[str] = None,
    ) -> Dict[str, str]:
        headers: Dict[str, str] = {
            "Host": host or "android15.prod.cloud.netflix.com",
            "Accept": "*/*",
            "User-Agent": user_agent or MSLAndroid.DEFAULT_USER_AGENT,
            "Accept-Language": language or "en-US",
            "Accept-Encoding": "gzip, deflate, br",
            "Content-Type": "application/json",
            "Connection": "keep-alive",
            "Content-Encoding": "msl_v1",
            "X-DeviceModel": device_model or MSLAndroid.DEFAULT_DEVICE_MODEL,
            "x-netflix.client.request.name": request_name,
            "x-netflix.request.attempt": "1",
            "x-netflix.request.id": "".join(random.choice("0123456789abcdef") for _ in range(32)),
            "x-netflix.request.client.context": MSLAndroid.DEFAULT_REQUEST_CONTEXT,
            "x-netflix.request.client.languages": "en-US",
            "x-netflix.request.client.timezoneid": "America/New_York",
            "x-netflix.clienttype": "samurai",
            "x-netflix.deviceformfactor": "PHONE",
            "x-netflix.devicememorylevel": "HIGH",
            "x-netflix.androidapi": "35",
            "x-netflix.context.os-version": "35",
            "x-netflix.context.form-factor": "phone",
            "x-netflix.context.ui-flavor": "android",
            "x-netflix.appver": "9.60.0",
            "x-netflix.context.app-version": "9.60.0",
            "x-netflix.esnprefix": "NFANDROID1-PRV-P-",
            "x-netflix.zuul.brotli.allowed": "true",
            "x-netflix.request.client.supportskidstop10": "true",
            "x-netflix.request.client.supportsgames": "true",
            "x-netflix.request.routing": '{"path":"\\/nq\\/android\\/playback\\/~1.0.0\\/router"}',
            "x-netflix.context.locales": "en-US",
            "x-netflix.context.android.installer-source": "com.android.vending",
        }
        if referer:
            headers["Referer"] = referer
        if viewable_id is not None:
            headers["x-netflix.playback.main-content-viewable-id"] = str(viewable_id)
        if profile_guid:
            headers["x-netflix.client.current-profile-guid"] = profile_guid
        if esn:
            headers["x-netflix.client.ftl.esn"] = esn
            headers["x-netflix.esn"] = esn
        if expiry_timeout is not None:
            headers["x-netflix.request.expiry.timeout"] = str(expiry_timeout)
        if extra_headers:
            headers.update(extra_headers)
        return headers

    @staticmethod
    def manifest_request_defaults() -> Tuple[str, Dict[str, str]]:
        return MSLAndroid.DEFAULT_MANIFEST_ENDPOINT, dict(MSLAndroid.DEFAULT_MANIFEST_PARAMS)

    @staticmethod
    def generate_msg_header(
        message_id: int,
        sender: str,
        is_handshake: bool,
        userauthdata: Optional[dict] = None,
        keyrequestdata: Optional[dict] = None,
        compression: Optional[str] = "GZIP",
    ) -> str:
        header_data: Dict[str, Any] = {
            "messageid": message_id,
            "renewable": True,
            "handshake": is_handshake,
            "capabilities": {
                "compressionalgos": [compression] if compression else [],
                "languages": ["en-US", "en"],
                "encoderformats": ["JSON"],
            },
            "timestamp": int(datetime.now(timezone.utc).timestamp()),
            "sender": sender,
            "nonreplayable": False,
            "recipient": "Netflix",
        }
        if userauthdata:
            header_data["userauthdata"] = userauthdata
        if keyrequestdata:
            header_data["keyrequestdata"] = [keyrequestdata]
        return jsonpickle.encode(header_data, unpicklable=False)

    @staticmethod
    def get_widevine_key(kid: bytes, keys: List[Any], permissions: List[str]) -> Optional[bytes]:
        import re
        normalized_perms = {re.sub(r'(?<!^)(?=[A-Z])', '_', p).lower() for p in permissions}
        for key in keys:
            if key.type != "OPERATOR_SESSION":
                continue
            key_perms = {p.lower() for p in (getattr(key, "permissions", None) or [])}
            if normalized_perms <= key_perms:
                return key.key
        return None

    def send_message(
        self,
        endpoint: str,
        params: Dict[str, str],
        application_data: Dict[str, Any],
        userauthdata: Optional[dict] = None,
        headers: Optional[dict] = None,
        proxy: Optional[Dict[str, str]] = None,
    ) -> Tuple[Dict[str, Any], Any]:
        normalized_application_data = self.normalize_application_data(endpoint, application_data)
        message = self.create_message(normalized_application_data, userauthdata)
        request_kwargs: Dict[str, Any] = {
            "url": endpoint,
            "data": message,
            "params": params,
            "headers": headers,
            "timeout": 30,
        }
        if proxy:
            request_kwargs["proxies"] = proxy

        res = self.session.post(**request_kwargs)

        if res.status_code != 200:
            raise RuntimeError(
                f"MSL request failed with HTTP {res.status_code}: {res.text[:500]}"
            )

        response_text = res.text or ""
        stripped_response = response_text.lstrip()
        if not stripped_response:
            raise RuntimeError("MSL request failed: empty response body")

        if not stripped_response.startswith("{"):
            content_type = res.headers.get("content-type", "")
            raise RuntimeError(
                "MSL request failed: the server did not return concatenated MSL JSON. "
                f"Content-Type: {content_type!r}. Body preview: {response_text[:500]!r}"
            )

        header, payload_data = self.parse_message(response_text)
        if not header:
            raise RuntimeError(
                f"MSL request failed: parsed response does not contain a header. Body preview: {response_text[:500]!r}"
            )

        if "errordata" in header:
            decoded_error = json.loads(
                base64.standard_b64decode(header["errordata"].encode("utf-8")).decode("utf-8")
            )
            raise RuntimeError(f"MSL response contains an error: {decoded_error}")

        return header, payload_data

    @classmethod
    def normalize_application_data(cls, endpoint: str, application_data: Any) -> Any:
        if not isinstance(application_data, dict):
            return application_data

        if cls._looks_like_wrapped_pbo_payload(application_data):
            return application_data

        route = cls._extract_pbo_route(application_data, endpoint)
        if route is None:
            return application_data

        common = dict(cls.DEFAULT_PBO_COMMON)
        if isinstance(application_data.get("common"), dict):
            common.update(application_data["common"])

        wrapped: Dict[str, Any] = {
            "version": application_data.get("version", cls.DEFAULT_PBO_VERSION),
            "common": common,
            "url": route,
            "languages": application_data.get("languages", list(cls.DEFAULT_PBO_LANGUAGES)),
            "params": application_data.get("params", {}),
        }

        for key in ("path", "method", "route", "endpoint"):
            wrapped.pop(key, None)

        for key, value in application_data.items():
            if key in wrapped or key in {"version", "common", "languages", "params", "path", "method", "route", "endpoint"}:
                continue
            wrapped[key] = value
        return wrapped

    @staticmethod
    def _looks_like_wrapped_pbo_payload(application_data: Dict[str, Any]) -> bool:
        return (
            "version" in application_data
            and "common" in application_data
            and "url" in application_data
            and "languages" in application_data
            and "params" in application_data
        )

    @staticmethod
    def _extract_pbo_route(application_data: Dict[str, Any], endpoint: str) -> Optional[str]:
        for key in ("url", "path", "route", "method", "endpoint"):
            value = application_data.get(key)
            if not isinstance(value, str) or not value.strip():
                continue
            value = value.strip()
            return value if value.startswith("/") else f"/{value}"

        endpoint_lower = endpoint.lower()
        if "manifest" in endpoint_lower:
            return "/manifest"
        if "pbo_tokens" in endpoint_lower or "pbo_config" in endpoint_lower:
            return None
        return None

    def create_message(self, application_data: Dict[str, Any], userauthdata: Optional[dict] = None) -> str:
        self.message_id += 1

        headerdata = self.encrypt(
            self.generate_msg_header(
                message_id=self.message_id,
                sender=self.sender,
                is_handshake=False,
                userauthdata=userauthdata,
            )
        )

        message = json.dumps(
            {
                "headerdata": base64.standard_b64encode(headerdata.encode("utf-8")).decode("utf-8"),
                "signature": self.sign(headerdata).decode("utf-8"),
                "mastertoken": self.keys.mastertoken,
            },
            separators=(",", ":"),
        )

        compressed_application_data = self.gzip_compress(
            json.dumps(application_data, separators=(",", ":")).encode("utf-8")
        ).decode("utf-8")
        payload_dicts = [
            {
                "sequencenumber": 1,
                "messageid": self.message_id,
                "compressionalgo": "GZIP",
                "data": compressed_application_data,
            },
            {
                "sequencenumber": 2,
                "messageid": self.message_id,
                "endofmsg": True,
                "data": "",
            },
        ]

        for payload_dict in payload_dicts:
            payload_chunk = self.encrypt(json.dumps(payload_dict, separators=(",", ":")))
            message += json.dumps(
                {
                    "payload": base64.standard_b64encode(payload_chunk.encode("utf-8")).decode("utf-8"),
                    "signature": self.sign(payload_chunk).decode("utf-8"),
                },
                separators=(",", ":"),
            )
        return message

    def decrypt_payload_chunks(self, payload_chunks: List[Dict[str, str]]) -> Any:
        raw_data = ""
        assert self.keys.encryption is not None

        for payload_chunk in payload_chunks:
            payload_chunk_json = json.loads(base64.standard_b64decode(payload_chunk["payload"]).decode("utf-8"))
            payload_decrypted = AES.new(
                key=self.keys.encryption,
                mode=AES.MODE_CBC,
                iv=base64.standard_b64decode(payload_chunk_json["iv"]),
            ).decrypt(base64.standard_b64decode(payload_chunk_json["ciphertext"]))
            payload_decrypted = Padding.unpad(payload_decrypted, 16)
            payload_decrypted_json = json.loads(payload_decrypted.decode("utf-8"))

            payload_data = base64.standard_b64decode(payload_decrypted_json["data"])
            if payload_decrypted_json.get("compressionalgo") == "GZIP":
                payload_data = zlib.decompress(payload_data, 16 + zlib.MAX_WBITS)
            raw_data += payload_data.decode("utf-8")

        if not raw_data:
            return None

        try:
            data = json.loads(raw_data)
        except Exception:
            return raw_data

        if "error" in data:
            return None
        if "result" not in data:
            return data
        return data["result"]

    @staticmethod
    def parse_concatenated_json(message: str) -> List[Dict[str, Any]]:
        decoder = json.JSONDecoder()
        items: List[Dict[str, Any]] = []
        index = 0
        length = len(message)

        while index < length:
            while index < length and message[index].isspace():
                index += 1
            if index >= length:
                break
            item, next_index = decoder.raw_decode(message, index)
            items.append(item)
            index = next_index
        return items

    def parse_message(self, message: str) -> Tuple[Dict[str, Any], Any]:
        parsed_message = self.parse_concatenated_json(message)
        header = parsed_message[0]
        encrypted_payload_chunks = parsed_message[1:] if len(parsed_message) > 1 else []
        payload_chunks = self.decrypt_payload_chunks(encrypted_payload_chunks) if encrypted_payload_chunks else {}
        return header, payload_chunks

    @staticmethod
    def gzip_compress(data: bytes) -> bytes:
        out = BytesIO()
        with gzip.GzipFile(fileobj=out, mode="w") as gzip_file:
            gzip_file.write(data)
        return base64.standard_b64encode(out.getvalue())

    @staticmethod
    def base64key_decode(payload: str) -> bytes:
        length = len(payload) % 4
        if length == 2:
            payload += "=="
        elif length == 3:
            payload += "="
        elif length != 0:
            raise ValueError("Invalid base64 string")
        return base64.urlsafe_b64decode(payload.encode("utf-8"))

    def encrypt(self, plaintext: str) -> str:
        if not self.keys.encryption:
            raise ValueError("Encryption key is not available")
        if not self.keys.mastertoken:
            raise ValueError("Master token is not available")

        iv = get_random_bytes(16)
        tokendata = json.loads(base64.standard_b64decode(self.keys.mastertoken["tokendata"]).decode("utf-8"))
        return json.dumps(
            {
                "ciphertext": base64.standard_b64encode(
                    AES.new(self.keys.encryption, AES.MODE_CBC, iv).encrypt(
                        Padding.pad(plaintext.encode("utf-8"), 16)
                    )
                ).decode("utf-8"),
                "keyid": f"{self.sender}_{tokendata['sequencenumber']}",
                "sha256": "AA==",
                "iv": base64.standard_b64encode(iv).decode("utf-8"),
            }
        )

    def sign(self, text: str) -> bytes:
        if not self.keys.sign:
            raise ValueError("Sign key is not available")
        return base64.standard_b64encode(HMAC.new(self.keys.sign, text.encode("utf-8"), SHA256).digest())

    @staticmethod
    def load_cache_data(msl_keys_path: Optional[Path] = None) -> Optional[MSLAndroidKeys]:
        if not msl_keys_path or not msl_keys_path.is_file():
            return None

        msl_keys = jsonpickle.decode(msl_keys_path.read_text(encoding="utf-8"))
        if msl_keys.mastertoken:
            tokendata = json.loads(base64.standard_b64decode(msl_keys.mastertoken["tokendata"]).decode("utf-8"))
            renewal_window = datetime.fromtimestamp(int(tokendata["renewalwindow"]), tz=timezone.utc)
            remaining_hours = (renewal_window - datetime.now(timezone.utc)).total_seconds() / 3600
            if remaining_hours < 10:
                return None
        return msl_keys

    @staticmethod
    def cache_keys(msl_keys: MSLAndroidKeys, msl_keys_path: Path) -> None:
        with open(msl_keys_path, "w", encoding="utf-8") as cache_file:
            cache_file.write(jsonpickle.encode(msl_keys, indent=4))
```

### `wpgskd\utils\MSL\__init__.py`

```python
import base64
import gzip
import json
import logging
import os
import random
import re
import sys
import time
import zlib
from datetime import datetime
from io import BytesIO

import jsonpickle
import requests
from Cryptodome.Cipher import AES, PKCS1_OAEP
from Cryptodome.Hash import HMAC, SHA256
from Cryptodome.PublicKey import RSA
from Cryptodome.Random import get_random_bytes
from Cryptodome.Util import Padding

from wpgskd.utils.MSL.MSLKeys import MSLKeys
from wpgskd.utils.MSL.schemes import EntityAuthenticationSchemes  # noqa: F401
from wpgskd.utils.MSL.schemes import KeyExchangeSchemes
from wpgskd.utils.MSL.schemes.EntityAuthentication import EntityAuthentication
from wpgskd.utils.MSL.schemes.KeyExchangeRequest import KeyExchangeRequest

class MSL:
    log = logging.getLogger("MSL")

    def __init__(self, session, endpoint, sender, keys, message_id, user_auth=None):
        self.session = session
        self.endpoint = endpoint
        self.sender = sender
        self.keys = keys
        self.user_auth = user_auth
        self.message_id = message_id

    @classmethod
    def handshake(cls, scheme, session, endpoint, sender, cdm=None, msl_keys_path=None):
        message_id = random.randint(0, pow(2, 52))
        msl_keys = MSL.load_cache_data(msl_keys_path)
        if msl_keys is not None:
            cls.log.info("Using cached MSL data")
        else:
            msl_keys = MSLKeys()
            if scheme != KeyExchangeSchemes.Widevine:
                msl_keys.rsa = RSA.generate(2048)

            if not cdm:
                raise cls.log.exit("- No cached data and no CDM specified")

            if not msl_keys_path:
                raise cls.log.exit("- No cached data and no MSL key path specified")

            if scheme == KeyExchangeSchemes.Widevine:
                msl_keys.cdm_session = cdm.open(
                    pssh=b"\x0A\x7A\x00\x6C\x38\x2B",
                    raw=True,
                    offline=True
                )
                keyrequestdata = KeyExchangeRequest.Widevine(
                    keyrequest=cdm.get_license_challenge(msl_keys.cdm_session)
                )
            else:
                keyrequestdata = KeyExchangeRequest.AsymmetricWrapped(
                    keypairid="superKeyPair",
                    mechanism="JWK_RSA",
                    publickey=msl_keys.rsa.publickey().exportKey(format="DER")
                )

            data = jsonpickle.encode({
                "entityauthdata": EntityAuthentication.Unauthenticated(sender),
                "headerdata": base64.b64encode(MSL.generate_msg_header(
                    message_id=message_id,
                    sender=sender,
                    is_handshake=True,
                    keyrequestdata=keyrequestdata
                ).encode("utf-8")).decode("utf-8"),
                "signature": ""
            }, unpicklable=False)
            data += json.dumps({
                "payload": base64.b64encode(json.dumps({
                    "messageid": message_id,
                    "data": "",
                    "sequencenumber": 1,
                    "endofmsg": True
                }).encode("utf-8")).decode("utf-8"),
                "signature": ""
            })

            try:
                r = session.post(
                    url=endpoint,
                    data=data
                )
            except requests.HTTPError as e:
                raise cls.log.exit(f"- Key exchange failed, response data is unexpected: {e.response.text}")

            key_exchange = r.json()
            if "errordata" in key_exchange:
                raise cls.log.exit("- Key exchange failed: " + json.loads(base64.b64decode(
                    key_exchange["errordata"]
                ).decode())["errormsg"])

            # parse the crypto keys
            key_response_data = json.JSONDecoder().decode(base64.b64decode(
                key_exchange["headerdata"]
            ).decode("utf-8"))["keyresponsedata"]

            if key_response_data["scheme"] != str(scheme):
                raise cls.log.exit("- Key exchange scheme mismatch occurred")

            key_data = key_response_data["keydata"]
            if scheme == KeyExchangeSchemes.Widevine:
                if hasattr(cdm, 'device') and isinstance(cdm.device, RemoteDevice):
                    msl_keys.encryption, msl_keys.sign = cdm.device.exchange(
                        cdm.sessions[msl_keys.cdm_session],
                        license_res=key_data["cdmkeyresponse"],
                        enc_key_id=base64.b64decode(key_data["encryptionkeyid"]),
                        hmac_key_id=base64.b64decode(key_data["hmackeyid"])
                    )
                    cdm.parse_license(msl_keys.cdm_session, key_data["cdmkeyresponse"])
                else:
                    cdm.parse_license(msl_keys.cdm_session, key_data["cdmkeyresponse"])
                    keys = cdm.get_keys(msl_keys.cdm_session)
                    msl_keys.encryption = MSL.get_widevine_key(
                        kid=base64.b64decode(key_data["encryptionkeyid"]),
                        keys=keys,
                        permissions=["AllowEncrypt", "AllowDecrypt"]
                    )
                    msl_keys.sign = MSL.get_widevine_key(
                        kid=base64.b64decode(key_data["hmackeyid"]),
                        keys=keys,
                        permissions=["AllowSign", "AllowSignatureVerify"]
                    )
            else:
                cipher_rsa = PKCS1_OAEP.new(msl_keys.rsa)
                msl_keys.encryption = MSL.base64key_decode(
                    json.JSONDecoder().decode(cipher_rsa.decrypt(
                        base64.b64decode(key_data["encryptionkey"])
                    ).decode("utf-8"))["k"]
                )
                msl_keys.sign = MSL.base64key_decode(
                    json.JSONDecoder().decode(cipher_rsa.decrypt(
                        base64.b64decode(key_data["hmackey"])
                    ).decode("utf-8"))["k"]
                )
            msl_keys.mastertoken = key_response_data["mastertoken"]

            MSL.cache_keys(msl_keys, msl_keys_path)
            cls.log.info("MSL handshake successful")
        return cls(
            session=session,
            endpoint=endpoint,
            sender=sender,
            keys=msl_keys,
            message_id=message_id
        )

    @staticmethod
    def load_cache_data(msl_keys_path=None):
        if not msl_keys_path or not os.path.exists(msl_keys_path):
            return None
        with open(msl_keys_path, encoding="utf-8") as fd:
            msl_keys = jsonpickle.decode(fd.read())
        if msl_keys.rsa:
            # noinspection PyTypeChecker
            # expects RsaKey, but is a string, this is because jsonpickle can't pickle RsaKey object
            # so as a workaround it exports to PEM, and then when reading, it imports that PEM back
            # to an RsaKey :)
            msl_keys.rsa = RSA.importKey(msl_keys.rsa)
        # If it's expired or close to, return None as it's unusable            
        if msl_keys.mastertoken and ((datetime.utcfromtimestamp(int(json.JSONDecoder().decode(
                base64.b64decode(msl_keys.mastertoken["tokendata"]).decode("utf-8")
        )["expiration"])) - datetime.now()).total_seconds() / 60 / 60) < 10:
            return None
        return msl_keys

    @staticmethod
    def cache_keys(msl_keys, msl_keys_path):
        os.makedirs(os.path.dirname(msl_keys_path), exist_ok=True)
        if msl_keys.rsa:
            # jsonpickle can't pickle RsaKey objects :(
            msl_keys.rsa = msl_keys.rsa.export_key()
        with open(msl_keys_path, "w", encoding="utf-8") as fd:
            fd.write(jsonpickle.encode(msl_keys))
        if msl_keys.rsa:
            # re-import now
            msl_keys.rsa = RSA.importKey(msl_keys.rsa)

    @staticmethod
    def generate_msg_header(message_id, sender, is_handshake, userauthdata=None, keyrequestdata=None,
                            compression="GZIP"):
        """
        The MSL header carries all MSL data used for entity and user authentication, message encryption
        and verification, and service tokens. Portions of the MSL header are encrypted.
        https://github.com/Netflix/msl/wiki/Messages#header-data

        :param message_id: number against which payload chunks are bound to protect against replay.
        :param sender: ESN
        :param is_handshake: This flag is set true if the message is a handshake message and will not include any
        payload chunks. It will include keyrequestdata.
        :param userauthdata: UserAuthData
        :param keyrequestdata: KeyRequestData
        :param compression: Supported compression algorithms.

        :return: The base64 encoded JSON String of the header
        """
        header_data = {
            "messageid": message_id,
            "renewable": True,  # MUST be True if is_handshake
            "handshake": is_handshake,
            "capabilities": {
                "compressionalgos": [compression] if compression else [],
                "languages": ["en-US"],  # bcp-47
                "encoderformats": ["JSON"]
            },
            "timestamp": int(time.time()),
            # undocumented or unused:
            "sender": sender,
            "nonreplayable": False,
            "recipient": "Netflix",
        }
        if userauthdata:
            header_data["userauthdata"] = userauthdata
        if keyrequestdata:
            header_data["keyrequestdata"] = [keyrequestdata]
        return jsonpickle.encode(header_data, unpicklable=False)

    @classmethod
    def get_widevine_key(cls, kid, keys, permissions):
        for key in keys:
            if key.kid != kid:
                continue
            if key.type != "OPERATOR_SESSION":
                cls.log.warning(f"Widevine Key Exchange: Wrong key type (not operator session) key {key}")
                continue
            if not set(permissions) <= set(key.permissions):
                cls.log.warning(f"Widevine Key Exchange: Incorrect permissions, key {key}, needed perms {permissions}")
                continue
            return key.key
        return None

    def send_message(self, endpoint, params, application_data, userauthdata=None):
        message = self.create_message(application_data, userauthdata)
        res = self.session.post(url=endpoint, data=message, params=params)
        header, payload_data = self.parse_message(res.text)
        if "errordata" in header:
            raise self.log.exit(
                "- MSL response message contains an error: {}".format(
                    json.loads(base64.b64decode(header["errordata"].encode("utf-8")).decode("utf-8"))
                )
            )
        return header, payload_data

    def create_message(self, application_data, userauthdata=None):
        self.message_id += 1  # new message must ue a new message id

        headerdata = self.encrypt(self.generate_msg_header(
            message_id=self.message_id,
            sender=self.sender,
            is_handshake=False,
            userauthdata=userauthdata
        ))

        header = json.dumps({
            "headerdata": base64.b64encode(headerdata.encode("utf-8")).decode("utf-8"),
            "signature": self.sign(headerdata).decode("utf-8"),
            "mastertoken": self.keys.mastertoken
        })

        payload_chunks = [self.encrypt(json.dumps({
            "messageid": self.message_id,
            "data": self.gzip_compress(json.dumps(application_data).encode("utf-8")).decode("utf-8"),
            "compressionalgo": "GZIP",
            "sequencenumber": 1,  # todo ; use sequence_number from master token instead?
            "endofmsg": True
        }))]

        message = header
        for payload_chunk in payload_chunks:
            message += json.dumps({
                "payload": base64.b64encode(payload_chunk.encode("utf-8")).decode("utf-8"),
                "signature": self.sign(payload_chunk).decode("utf-8")
            })

        return message

    def decrypt_payload_chunks(self, payload_chunks):
        """
        Decrypt and extract data from payload chunks

        :param payload_chunks: List of payload chunks
        :return: json object
        """
        raw_data = ""

        for payload_chunk in payload_chunks:
            # todo ; verify signature of payload_chunk["signature"] against payload_chunk["payload"]
            # expecting base64-encoded json string
            payload_chunk = json.loads(base64.b64decode(payload_chunk["payload"]).decode("utf-8"))
            # decrypt the payload
            payload_decrypted = AES.new(
                key=self.keys.encryption,
                mode=AES.MODE_CBC,
                iv=base64.b64decode(payload_chunk["iv"])
            ).decrypt(base64.b64decode(payload_chunk["ciphertext"]))
            payload_decrypted = Padding.unpad(payload_decrypted, 16)
            payload_decrypted = json.loads(payload_decrypted.decode("utf-8"))
            # decode and uncompress data if compressed
            payload_data = base64.b64decode(payload_decrypted["data"])
            if payload_decrypted.get("compressionalgo") == "GZIP":
                payload_data = zlib.decompress(payload_data, 16 + zlib.MAX_WBITS)
            raw_data += payload_data.decode("utf-8")

        data = json.loads(raw_data)
        if "error" in data:
            error = data["error"]
            error_display = error.get("display")
            error_detail = re.sub(r" \(E3-[^)]+\)", "", error.get("detail", ""))

            if error_display:
                self.log.critical(f"- {error_display}")
            if error_detail:
                self.log.critical(f"- {error_detail}")

            if not (error_display or error_detail):
                self.log.critical(f"- {error}")

            sys.exit(1)

        return data["result"]

    def parse_message(self, message):
        """
        Parse an MSL message into a header and list of payload chunks

        :param message: MSL message
        :returns: a 2-item tuple containing message and list of payload chunks if available
        """
        parsed_message = json.loads("[{}]".format(message.replace("}{", "},{")))

        header = parsed_message[0]
        encrypted_payload_chunks = parsed_message[1:] if len(parsed_message) > 1 else []
        if encrypted_payload_chunks:
            payload_chunks = self.decrypt_payload_chunks(encrypted_payload_chunks)
        else:
            payload_chunks = {}

        return header, payload_chunks

    @staticmethod
    def gzip_compress(data):
        out = BytesIO()
        with gzip.GzipFile(fileobj=out, mode="w") as fd:
            fd.write(data)
        return base64.b64encode(out.getvalue())

    @staticmethod
    def base64key_decode(payload):
        length = len(payload) % 4
        if length == 2:
            payload += "=="
        elif length == 3:
            payload += "="
        elif length != 0:
            raise ValueError("Invalid base64 string")
        return base64.urlsafe_b64decode(payload.encode("utf-8"))

    def encrypt(self, plaintext):
        """
        Encrypt the given Plaintext with the encryption key
        :param plaintext:
        :return: Serialized JSON String of the encryption Envelope
        """
        iv = get_random_bytes(16)
        return json.dumps({
            "ciphertext": base64.b64encode(
                AES.new(
                    self.keys.encryption,
                    AES.MODE_CBC,
                    iv
                ).encrypt(
                    Padding.pad(plaintext.encode("utf-8"), 16)
                )
            ).decode("utf-8"),
            "keyid": "{}_{}".format(self.sender, json.loads(
                base64.b64decode(self.keys.mastertoken["tokendata"]).decode("utf-8")
            )["sequencenumber"]),
            "sha256": "AA==",
            "iv": base64.b64encode(iv).decode("utf-8")
        })

    def sign(self, text):
        """
        Calculates the HMAC signature for the given text with the current sign key and SHA256
        :param text:
        :return: Base64 encoded signature
        """
        return base64.b64encode(HMAC.new(self.keys.sign, text.encode("utf-8"), SHA256).digest())
```

### `wpgskd\utils\MSL\schemes\EntityAuthentication.py`

```python
from wpgskd.utils.MSL import EntityAuthenticationSchemes
from wpgskd.utils.MSL.MSLObject import MSLObject


# noinspection PyPep8Naming
class EntityAuthentication(MSLObject):
    def __init__(self, scheme, authdata):
        """
        Data used to identify and authenticate the entity associated with a message.
        https://github.com/Netflix/msl/wiki/Entity-Authentication-%28Configuration%29

        :param scheme: Entity Authentication Scheme identifier
        :param authdata: Entity Authentication data
        """
        self.scheme = str(scheme)
        self.authdata = authdata

    @classmethod
    def Unauthenticated(cls, identity):
        """
        The unauthenticated entity authentication scheme does not provide encryption or authentication and only
        identifies the entity. Therefore entity identities can be harvested and spoofed. The benefit of this
        authentication scheme is that the entity has control over its identity. This may be useful if the identity is
        derived from or related to other data, or if retaining the identity is desired across state resets or in the
        event of MSL errors requiring entity re-authentication.
        """
        return cls(
            scheme=EntityAuthenticationSchemes.Unauthenticated,
            authdata={"identity": identity}
        )

    @classmethod
    def Widevine(cls, devtype, keyrequest):
        """
        The Widevine entity authentication scheme is used by devices with the Widevine CDM. It does not provide
        encryption or authentication and only identifies the entity. Therefore entity identities can be harvested
        and spoofed. The entity identity is composed from the provided device type and Widevine key request data. The
        Widevine CDM properties can be extracted from the key request data.

        When coupled with the Widevine key exchange scheme, the entity identity can be cryptographically validated by
        comparing the entity authentication key request data against the key exchange key request data.

        Note that the local entity will not know its entity identity when using this scheme.

        > Devtype

        An arbitrary value identifying the device type the local entity wishes to assume. The data inside the Widevine
        key request may be optionally used to validate the claimed device type.

        :param devtype: Local entity device type
        :param keyrequest: Widevine key request
        """
        return cls(
            scheme=EntityAuthenticationSchemes.Widevine,
            authdata={
                "devtype": devtype,
                "keyrequest": keyrequest
            }
        )
```

### `wpgskd\utils\MSL\schemes\KeyExchangeRequest.py`

```python
import base64

from wpgskd.utils.MSL import KeyExchangeSchemes
from wpgskd.utils.MSL.MSLObject import MSLObject


# noinspection PyPep8Naming
class KeyExchangeRequest(MSLObject):
    def __init__(self, scheme, keydata):
        """
        Session key exchange data from a requesting entity.
        https://github.com/Netflix/msl/wiki/Key-Exchange-%28Configuration%29

        :param scheme: Key Exchange Scheme identifier
        :param keydata: Key Request data
        """
        self.scheme = str(scheme)
        self.keydata = keydata

    @classmethod
    def AsymmetricWrapped(cls, keypairid, mechanism, publickey):
        """
        Asymmetric wrapped key exchange uses a generated ephemeral asymmetric key pair for key exchange. It will
        typically be used when there is no other data or keys from which to base secure key exchange.

        This mechanism provides perfect forward secrecy but does not guarantee that session keys will only be available
        to the requesting entity if the requesting MSL stack has been modified to perform the operation on behalf of a
        third party.

        > Key Pair ID

        The key pair ID is included as a sanity check.

        > Mechanism & Public Key

        The following mechanisms are associated public key formats are currently supported.

            Field 	    Public  Key Format 	Description
            RSA 	    SPKI 	RSA-OAEP    encrypt/decrypt
            ECC 	    SPKI 	ECIES       encrypt/decrypt
            JWEJS_RSA 	SPKI 	RSA-OAEP    JSON Web Encryption JSON Serialization
            JWE_RSA 	SPKI 	RSA-OAEP    JSON Web Encryption Compact Serialization
            JWK_RSA 	SPKI 	RSA-OAEP    JSON Web Key
            JWK_RSAES 	SPKI 	RSA PKCS#1  JSON Web Key

        :param keypairid: key pair ID
        :param mechanism: asymmetric key type
        :param publickey: public key
        """
        return cls(
            scheme=KeyExchangeSchemes.AsymmetricWrapped,
            keydata={
                "keypairid": keypairid,
                "mechanism": mechanism,
                "publickey": base64.b64encode(publickey).decode("utf-8")
            }
        )

    @classmethod
    def Widevine(cls, keyrequest):
        """
        Google Widevine provides a secure key exchange mechanism. When requested the Widevine component will issue a
        one-time use key request. The Widevine server library can be used to authenticate the request and return
        randomly generated symmetric keys in a protected key response bound to the request and Widevine client library.
        The key response also specifies the key identities, types and their permitted usage.

        The Widevine key request also contains a model identifier and a unique device identifier with an expectation of
        long-term persistence. These values are available from the Widevine client library and can be retrieved from
        the key request by the Widevine server library.

        The Widevine client library will protect the returned keys from inspection or misuse.

        :param keyrequest: Base64-encoded Widevine CDM license challenge (PSSH: b'\x0A\x7A\x00\x6C\x38\x2B')
        """
        if not isinstance(keyrequest, str):
            keyrequest = base64.b64encode(keyrequest).decode()
        return cls(
            scheme=KeyExchangeSchemes.Widevine,
            keydata={"keyrequest": keyrequest}
        )
```

### `wpgskd\utils\MSL\schemes\PlayReadyKeyExchangeScheme.py`

```python
import base64
import json
import os
from Cryptodome.Cipher import AES, PKCS1_OAEP
from Cryptodome.Hash import HMAC, SHA256
from Cryptodome.Random import get_random_bytes
from Cryptodome.Util import Padding

from wpgskd.utils.MSL.schemes.KeyExchangeRequest import KeyExchangeRequest

class PlayReady(KeyExchangeRequest):
    """
    Implementation of the PlayReady Key Exchange Scheme for MSL.
    """
    
    def __init__(self):
        self.encryption_key = None
        self.sign_key = None
        self.sender = None
    
    def perform_key_exchange(self, session, endpoint, sender, cdm):
        """
        Performs a key exchange using PlayReady.
        
        Parameters:
            session: HTTP session with necessary cookies
            endpoint: Endpoint for key exchange
            sender: ESN of the device
            cdm: CDM instance
        """
        self.sender = sender
        
        # Generate random keys for encryption and signing
        self.encryption_key = get_random_bytes(16)  # AES-128
        self.sign_key = get_random_bytes(32)  # HMAC-SHA256
        
        # Return keys in the format required by MSL
        return {
            "encryptionkey": base64.b64encode(self.encryption_key).decode("utf-8"),
            "hmackey": base64.b64encode(self.sign_key).decode("utf-8")
        }
    
    def encrypt(self, data, encryption_envelope=None):
        """
        Encrypts data using the encryption key.
        
        Parameters:
            data: Data to encrypt
            encryption_envelope: Not used in PlayReady
        """
        if not self.encryption_key:
            raise ValueError("No encryption key available")
        
        # Generate a random IV
        iv = get_random_bytes(16)
        
        # Encrypt the data
        cipher = AES.new(self.encryption_key, AES.MODE_CBC, iv)
        ciphertext = cipher.encrypt(Padding.pad(data.encode("utf-8"), 16))
        
        # Return encrypted data in the format required by MSL
        return {
            "keyid": self.sender,
            "iv": base64.b64encode(iv).decode("utf-8"),
            "ciphertext": base64.b64encode(ciphertext).decode("utf-8")
        }
    
    def decrypt(self, data):
        """
        Decrypts data using the encryption key.
        
        Parameters:
            data: Encrypted data (with iv and ciphertext)
        """
        if not self.encryption_key:
            raise ValueError("No encryption key available")
        
        # Decode IV and ciphertext
        iv = base64.b64decode(data["iv"])
        ciphertext = base64.b64decode(data["ciphertext"])
        
        # Decrypt the data
        cipher = AES.new(self.encryption_key, AES.MODE_CBC, iv)
        plaintext = Padding.unpad(cipher.decrypt(ciphertext), 16)
        
        return plaintext
    
    def sign(self, data):
        """
        Signs data using the sign key.
        
        Parameters:
            data: Data to sign
        """
        if not self.sign_key:
            raise ValueError("No sign key available")
        
        # Sign the data with HMAC-SHA256
        signature = HMAC.new(self.sign_key, data.encode("utf-8"), SHA256).digest()
        return base64.b64encode(signature)
    
    def verify(self, data, signature):
        """
        Verifies a signature.
        
        Parameters:
            data: Data that was signed
            signature: Signature to verify
        """
        expected_signature = self.sign(data)
        return signature == expected_signature.decode("utf-8")
```

### `wpgskd\utils\MSL\schemes\UserAuthentication.py`

```python
from wpgskd.utils.MSL.MSLObject import MSLObject
from wpgskd.utils.MSL.schemes import UserAuthenticationSchemes


# noinspection PyPep8Naming
class UserAuthentication(MSLObject):
    def __init__(self, scheme, authdata):
        """
        Data used to identify and authenticate the user associated with a message.
        https://github.com/Netflix/msl/wiki/User-Authentication-%28Configuration%29

        :param scheme: User Authentication Scheme identifier
        :param authdata: User Authentication data
        """
        self.scheme = str(scheme)
        self.authdata = authdata

    @classmethod
    def EmailPassword(cls, email, password):
        """
        Email and password is a standard user authentication scheme in wide use.

        :param email: user email address
        :param password: user password
        """
        return cls(
            scheme=UserAuthenticationSchemes.EmailPassword,
            authdata={
                "email": email,
                "password": password
            }
        )

    @classmethod
    def NetflixIDCookies(cls, netflixid, securenetflixid):
        """
        Netflix ID HTTP cookies are used when the user has previously logged in to a web site. Possession of the
        cookies serves as proof of user identity, in the same manner as they do when communicating with the web site.

        The Netflix ID cookie and Secure Netflix ID cookie are HTTP cookies issued by the Netflix web site after
        subscriber login. The Netflix ID cookie is encrypted and identifies the subscriber and analogous to a
        subscriber’s username. The Secure Netflix ID cookie is tied to a Netflix ID cookie and only sent over HTTPS
        and analogous to a subscriber’s password.

        In some cases the Netflix ID and Secure Netflix ID cookies will be unavailable to the MSL stack or application.
        If either or both of the Netflix ID or Secure Netflix ID cookies are absent in the above data structure the
        HTTP cookie headers will be queried for it; this is only acceptable when HTTPS is used as the underlying
        transport protocol.

        :param netflixid: Netflix ID cookie
        :param securenetflixid: Secure Netflix ID cookie
        """
        return cls(
            scheme=UserAuthenticationSchemes.NetflixIDCookies,
            authdata={
                "netflixid": netflixid,
                "securenetflixid": securenetflixid
            }
        )
```

### `wpgskd\utils\MSL\schemes\__init__.py`

```python
from enum import Enum


class Scheme(Enum):
    def __str__(self):
        return str(self.value)


class EntityAuthenticationSchemes(Scheme):
    """https://github.com/Netflix/msl/wiki/Entity-Authentication-%28Configuration%29"""
    Unauthenticated = "NONE"
    Widevine = "WIDEVINE"


class UserAuthenticationSchemes(Scheme):
    """https://github.com/Netflix/msl/wiki/User-Authentication-%28Configuration%29"""
    EmailPassword = "EMAIL_PASSWORD"
    NetflixIDCookies = "NETFLIXID"


class KeyExchangeSchemes(Scheme):
    """https://github.com/Netflix/msl/wiki/Key-Exchange-%28Configuration%29"""
    AsymmetricWrapped = "ASYMMETRIC_WRAPPED"
    Widevine = "WIDEVINE"
```

### `wpgskd\vendor\__init__.py`

```python

```

### `wpgskd\vendor\pymp4\__init__.py`

```python

```

### `wpgskd\vendor\pymp4\cli.py`

```python
#!/usr/bin/env python
from __future__ import print_function
import io
import logging
import argparse

from pymp4.parser import Box
from construct import setglobalfullprinting

log = logging.getLogger(__name__)
setglobalfullprinting(True)


def dump():
    parser = argparse.ArgumentParser(description='Dump all the boxes from an MP4 file')
    parser.add_argument("input_file", type=argparse.FileType("rb"), metavar="FILE", help="Path to the MP4 file to open")

    args = parser.parse_args()

    fd = args.input_file
    fd.seek(0, io.SEEK_END)
    eof = fd.tell()
    fd.seek(0)

    while fd.tell() < eof:
        box = Box.parse_stream(fd)
        print(box)
```

### `wpgskd\vendor\pymp4\exceptions.py`

```python
#!/usr/bin/env python
"""
   Copyright 2016 beardypig

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
"""


class BoxNotFound(Exception):
    pass
```

### `wpgskd\vendor\pymp4\parser.py`

```python
#!/usr/bin/env python
"""
   Copyright 2016 beardypig

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
"""
import logging
from uuid import UUID

from construct import *
import construct.core
from construct.lib import *

log = logging.getLogger(__name__)

UNITY_MATRIX = [0x10000, 0, 0, 0, 0x10000, 0, 0, 0, 0x40000000]


class PrefixedIncludingSize(Subconstruct):
    __slots__ = ["name", "lengthfield", "subcon"]

    def __init__(self, lengthfield, subcon):
        super(PrefixedIncludingSize, self).__init__(subcon)
        self.lengthfield = lengthfield

    def _parse(self, stream, context, path):
        try:
            lengthfield_size = self.lengthfield.sizeof()
            length = self.lengthfield._parse(stream, context, path)
        except SizeofError:
            offset_start = stream.tell()
            length = self.lengthfield._parse(stream, context, path)
            lengthfield_size = stream.tell() - offset_start

        stream2 = BoundBytesIO(stream, length - lengthfield_size)
        obj = self.subcon._parse(stream2, context, path)
        return obj

    def _build(self, obj, stream, context, path):
        try:
            # needs to be both fixed size, seekable and tellable (third not checked)
            self.lengthfield.sizeof()
            if not stream.seekable:
                raise SizeofError
            offset_start = stream.tell()
            self.lengthfield._build(0, stream, context, path)
            self.subcon._build(obj, stream, context, path)
            offset_end = stream.tell()
            stream.seek(offset_start)
            self.lengthfield._build(offset_end - offset_start, stream, context, path)
            stream.seek(offset_end)
        except SizeofError:
            data = self.subcon.build(obj, context)
            sl, p_sl = 0, 0
            dlen = len(data)
            # do..while
            i = 0
            while True:
                i += 1
                p_sl = sl
                sl = len(self.lengthfield.build(dlen + sl))
                if p_sl == sl: break

                self.lengthfield._build(dlen + sl, stream, context, path)
            else:
                self.lengthfield._build(len(data), stream, context, path)
            construct.core._write_stream(stream, len(data), data)

    def _sizeof(self, context, path):
        return self.lengthfield._sizeof(context, path) + self.subcon._sizeof(context, path)


# Header box

FileTypeBox = Struct(
    "type" / Const(b"ftyp"),
    "major_brand" / String(4),
    "minor_version" / Int32ub,
    "compatible_brands" / GreedyRange(String(4)),
)

SegmentTypeBox = Struct(
    "type" / Const(b"styp"),
    "major_brand" / String(4),
    "minor_version" / Int32ub,
    "compatible_brands" / GreedyRange(String(4)),
)

# Catch find boxes

RawBox = Struct(
    "type" / String(4, padchar=b" ", paddir="right"),
    "data" / Default(GreedyBytes, b"")
)

FreeBox = Struct(
    "type" / Const(b"free"),
    "data" / GreedyBytes
)

SkipBox = Struct(
    "type" / Const(b"skip"),
    "data" / GreedyBytes
)

# Movie boxes, contained in a moov Box

MovieHeaderBox = Struct(
    "type" / Const(b"mvhd"),
    "version" / Default(Int8ub, 0),
    "flags" / Default(Int24ub, 0),
    Embedded(Switch(this.version, {
        1: Struct(
            "creation_time" / Default(Int64ub, 0),
            "modification_time" / Default(Int64ub, 0),
            "timescale" / Default(Int32ub, 10000000),
            "duration" / Int64ub
        ),
        0: Struct(
            "creation_time" / Default(Int32ub, 0),
            "modification_time" / Default(Int32ub, 0),
            "timescale" / Default(Int32ub, 10000000),
            "duration" / Int32ub,
        ),
    })),
    "rate" / Default(Int32sb, 65536),
    "volume" / Default(Int16sb, 256),
    # below could be just Padding(10) but why not
    Const(Int16ub, 0),
    Const(Int32ub, 0),
    Const(Int32ub, 0),
    "matrix" / Default(Int32sb[9], UNITY_MATRIX),
    "pre_defined" / Default(Int32ub[6], [0] * 6),
    "next_track_ID" / Default(Int32ub, 0xffffffff)
)

# Track boxes, contained in trak box

TrackHeaderBox = Struct(
    "type" / Const(b"tkhd"),
    "version" / Default(Int8ub, 0),
    "flags" / Default(Int24ub, 1),
    Embedded(Switch(this.version, {
        1: Struct(
            "creation_time" / Default(Int64ub, 0),
            "modification_time" / Default(Int64ub, 0),
            "track_ID" / Default(Int32ub, 1),
            Padding(4),
            "duration" / Default(Int64ub, 0),
        ),
        0: Struct(
            "creation_time" / Default(Int32ub, 0),
            "modification_time" / Default(Int32ub, 0),
            "track_ID" / Default(Int32ub, 1),
            Padding(4),
            "duration" / Default(Int32ub, 0),
        ),
    })),
    Padding(8),
    "layer" / Default(Int16sb, 0),
    "alternate_group" / Default(Int16sb, 0),
    "volume" / Default(Int16sb, 0),
    Padding(2),
    "matrix" / Default(Array(9, Int32sb), UNITY_MATRIX),
    "width" / Default(Int32ub, 0),
    "height" / Default(Int32ub, 0),
)

HDSSegmentBox = Struct(
    "type" / Const(b"abst"),
    "version" / Default(Int8ub, 0),
    "flags" / Default(Int24ub, 0),
    "info_version" / Int32ub,
    EmbeddedBitStruct(
        Padding(1),
        "profile" / Flag,
        "live" / Flag,
        "update" / Flag,
        Padding(4)
    ),
    "time_scale" / Int32ub,
    "current_media_time" / Int64ub,
    "smpte_time_code_offset" / Int64ub,
    "movie_identifier" / CString(),
    "server_entry_table" / PrefixedArray(Int8ub, CString()),
    "quality_entry_table" / PrefixedArray(Int8ub, CString()),
    "drm_data" / CString(),
    "metadata" / CString(),
    "segment_run_table" / PrefixedArray(Int8ub, LazyBound(lambda x: Box)),
    "fragment_run_table" / PrefixedArray(Int8ub, LazyBound(lambda x: Box))
)

HDSSegmentRunBox = Struct(
    "type" / Const(b"asrt"),
    "version" / Default(Int8ub, 0),
    "flags" / Default(Int24ub, 0),
    "quality_entry_table" / PrefixedArray(Int8ub, CString()),
    "segment_run_enteries" / PrefixedArray(Int32ub, Struct(
        "first_segment" / Int32ub,
        "fragments_per_segment" / Int32ub
    ))
)

HDSFragmentRunBox = Struct(
    "type" / Const(b"afrt"),
    "version" / Default(Int8ub, 0),
    "flags" / BitStruct(
        Padding(23),
        "update" / Flag
    ),
    "time_scale" / Int32ub,
    "quality_entry_table" / PrefixedArray(Int8ub, CString()),
    "fragment_run_enteries" / PrefixedArray(Int32ub, Struct(
        "first_fragment" / Int32ub,
        "first_fragment_timestamp" / Int64ub,
        "fragment_duration" / Int32ub,
        "discontinuity" / If(this.fragment_duration == 0, Int8ub)
    ))
)


# Boxes contained by Media Box

class ISO6392TLanguageCode(Adapter):
    def _decode(self, obj, context):
        """
        Get the python representation of the obj
        """
        return b''.join(map(int2byte, [c + 0x60 for c in bytearray(obj)])).decode("utf8")

    def _encode(self, obj, context):
        """
        Get the bytes representation of the obj
        """
        return [c - 0x60 for c in bytearray(obj.encode("utf8"))]


MediaHeaderBox = Struct(
    "type" / Const(b"mdhd"),
    "version" / Default(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "creation_time" / IfThenElse(this.version == 1, Int64ub, Int32ub),
    "modification_time" / IfThenElse(this.version == 1, Int64ub, Int32ub),
    "timescale" / Int32ub,
    "duration" / IfThenElse(this.version == 1, Int64ub, Int32ub),
    Embedded(BitStruct(
        Padding(1),
        "language" / ISO6392TLanguageCode(BitsInteger(5)[3]),
    )),
    Padding(2, pattern=b"\x00"),
)

HandlerReferenceBox = Struct(
    "type" / Const(b"hdlr"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    Padding(4, pattern=b"\x00"),
    "handler_type" / String(4),
    Padding(12, pattern=b"\x00"),  # Int32ub[3]
    "name" / CString(encoding="utf8")
)

# Boxes contained by Media Info Box

VideoMediaHeaderBox = Struct(
    "type" / Const(b"vmhd"),
    "version" / Default(Int8ub, 0),
    "flags" / Const(Int24ub, 1),
    "graphics_mode" / Default(Int16ub, 0),
    "opcolor" / Struct(
        "red" / Default(Int16ub, 0),
        "green" / Default(Int16ub, 0),
        "blue" / Default(Int16ub, 0),
    ),
)

DataEntryUrlBox = PrefixedIncludingSize(Int32ub, Struct(
    "type" / Const(b"url "),
    "version" / Const(Int8ub, 0),
    "flags" / BitStruct(
        Padding(23), "self_contained" / Rebuild(Flag, ~this._.location)
    ),
    "location" / If(~this.flags.self_contained, CString(encoding="utf8")),
))

DataEntryUrnBox = PrefixedIncludingSize(Int32ub, Struct(
    "type" / Const(b"urn "),
    "version" / Const(Int8ub, 0),
    "flags" / BitStruct(
        Padding(23), "self_contained" / Rebuild(Flag, ~(this._.name & this._.location))
    ),
    "name" / If(this.flags == 0, CString(encoding="utf8")),
    "location" / If(this.flags == 0, CString(encoding="utf8")),
))

DataReferenceBox = Struct(
    "type" / Const(b"dref"),
    "version" / Const(Int8ub, 0),
    "flags" / Default(Int24ub, 0),
    "data_entries" / PrefixedArray(Int32ub, Select(DataEntryUrnBox, DataEntryUrlBox)),
)

# Sample Table boxes (stbl)

MP4ASampleEntryBox = Struct(
    "version" / Default(Int16ub, 0),
    "revision" / Const(Int16ub, 0),
    "vendor" / Const(Int32ub, 0),
    "channels" / Default(Int16ub, 2),
    "bits_per_sample" / Default(Int16ub, 16),
    "compression_id" / Default(Int16sb, 0),
    "packet_size" / Const(Int16ub, 0),
    "sampling_rate" / Int16ub,
    Padding(2)
)


class MaskedInteger(Adapter):
    def _decode(self, obj, context):
        return obj & 0x1F

    def _encode(self, obj, context):
        return obj & 0x1F


AAVC = Struct(
    "version" / Const(Int8ub, 1),
    "profile" / Int8ub,
    "compatibility" / Int8ub,
    "level" / Int8ub,
    EmbeddedBitStruct(
        Padding(6, pattern=b'\x01'),
        "nal_unit_length_field" / Default(BitsInteger(2), 3),
    ),
    "sps" / Default(PrefixedArray(MaskedInteger(Int8ub), PascalString(Int16ub)), []),
    "pps" / Default(PrefixedArray(Int8ub, PascalString(Int16ub)), [])
)

HVCC = Struct(
    EmbeddedBitStruct(
        "version" / Const(BitsInteger(8), 1),
        "profile_space" / BitsInteger(2),
        "general_tier_flag" / BitsInteger(1),
        "general_profile" / BitsInteger(5),
        "general_profile_compatibility_flags" / BitsInteger(32),
        "general_constraint_indicator_flags" / BitsInteger(48),
        "general_level" / BitsInteger(8),
        Padding(4, pattern=b'\xff'),
        "min_spatial_segmentation" / BitsInteger(12),
        Padding(6, pattern=b'\xff'),
        "parallelism_type" / BitsInteger(2),
        Padding(6, pattern=b'\xff'),
        "chroma_format" / BitsInteger(2),
        Padding(5, pattern=b'\xff'),
        "luma_bit_depth" / BitsInteger(3),
        Padding(5, pattern=b'\xff'),
        "chroma_bit_depth" / BitsInteger(3),
        "average_frame_rate" / BitsInteger(16),
        "constant_frame_rate" / BitsInteger(2),
        "num_temporal_layers" / BitsInteger(3),
        "temporal_id_nested" / BitsInteger(1),
        "nalu_length_size" / BitsInteger(2),
    ),
    # TODO: parse NALUs
    "raw_bytes" / GreedyBytes
)

AVC1SampleEntryBox = Struct(
    "version" / Default(Int16ub, 0),
    "revision" / Const(Int16ub, 0),
    "vendor" / Default(String(4, padchar=b" "), b"brdy"),
    "temporal_quality" / Default(Int32ub, 0),
    "spatial_quality" / Default(Int32ub, 0),
    "width" / Int16ub,
    "height" / Int16ub,
    "horizontal_resolution" / Default(Int16ub, 72),  # TODO: actually a fixed point decimal
    Padding(2),
    "vertical_resolution" / Default(Int16ub, 72),  # TODO: actually a fixed point decimal
    Padding(2),
    "data_size" / Const(Int32ub, 0),
    "frame_count" / Default(Int16ub, 1),
    "compressor_name" / Default(String(32, padchar=b" "), ""),
    "depth" / Default(Int16ub, 24),
    "color_table_id" / Default(Int16sb, -1),
    "avc_data" / PrefixedIncludingSize(Int32ub, Struct(
    "type" / String(4, padchar=b" ", paddir="right"),
        Embedded(Switch(this.type, {
            b"avcC": AAVC,
            b"hvcC": HVCC,
        }, Struct("data" / GreedyBytes)))
    )),
    "sample_info" / LazyBound(lambda _: GreedyRange(Box))
)

SampleEntryBox = PrefixedIncludingSize(Int32ub, Struct(
    "format" / String(4, padchar=b" ", paddir="right"),
    Padding(6, pattern=b"\x00"),
    "data_reference_index" / Default(Int16ub, 1),
    Embedded(Switch(this.format, {
        b"ec-3": MP4ASampleEntryBox,
        b"mp4a": MP4ASampleEntryBox,
        b"enca": MP4ASampleEntryBox,
        b"avc1": AVC1SampleEntryBox,
        b"encv": AVC1SampleEntryBox,
        b"wvtt": Struct("children" / LazyBound(lambda ctx: GreedyRange(Box)))
    }, Struct("data" / GreedyBytes)))
))

BitRateBox = Struct(
    "type" / Const(b"btrt"),
    "bufferSizeDB" / Int32ub,
    "maxBitrate" / Int32ub,
    "avgBirate" / Int32ub,
)

SampleDescriptionBox = Struct(
    "type" / Const(b"stsd"),
    "version" / Default(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "entries" / PrefixedArray(Int32ub, SampleEntryBox)
)

SampleSizeBox = Struct(
    "type" / Const(b"stsz"),
    "version" / Int8ub,
    "flags" / Const(Int24ub, 0),
    "sample_size" / Int32ub,
    "sample_count" / Int32ub,
    "entry_sizes" / If(this.sample_size == 0, Array(this.sample_count, Int32ub))
)

SampleSizeBox2 = Struct(
    "type" / Const(b"stz2"),
    "version" / Int8ub,
    "flags" / Const(Int24ub, 0),
    Padding(3, pattern=b"\x00"),
    "field_size" / Int8ub,
    "sample_count" / Int24ub,
    "entries" / Array(this.sample_count, Struct(
        "entry_size" / LazyBound(lambda ctx: globals()["Int%dub" % ctx.field_size])
    ))
)

SampleDegradationPriorityBox = Struct(
    "type" / Const(b"stdp"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
)

TimeToSampleBox = Struct(
    "type" / Const(b"stts"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "entries" / Default(PrefixedArray(Int32ub, Struct(
        "sample_count" / Int32ub,
        "sample_delta" / Int32ub,
    )), [])
)

SyncSampleBox = Struct(
    "type" / Const(b"stss"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "entries" / Default(PrefixedArray(Int32ub, Struct(
        "sample_number" / Int32ub,
    )), [])
)

SampleToChunkBox = Struct(
    "type" / Const(b"stsc"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "entries" / Default(PrefixedArray(Int32ub, Struct(
        "first_chunk" / Int32ub,
        "samples_per_chunk" / Int32ub,
        "sample_description_index" / Int32ub,
    )), [])
)

ChunkOffsetBox = Struct(
    "type" / Const(b"stco"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "entries" / Default(PrefixedArray(Int32ub, Struct(
        "chunk_offset" / Int32ub,
    )), [])
)

ChunkLargeOffsetBox = Struct(
    "type" / Const(b"co64"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "entries" / PrefixedArray(Int32ub, Struct(
        "chunk_offset" / Int64ub,
    ))
)

# Movie Fragment boxes, contained in moof box

MovieFragmentHeaderBox = Struct(
    "type" / Const(b"mfhd"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "sequence_number" / Int32ub
)

TrackFragmentBaseMediaDecodeTimeBox = Struct(
    "type" / Const(b"tfdt"),
    "version" / Int8ub,
    "flags" / Const(Int24ub, 0),
    "baseMediaDecodeTime" / Switch(this.version, {1: Int64ub, 0: Int32ub})
)

TrackSampleFlags = BitStruct(
    Padding(4),
    "is_leading" / Default(Enum(BitsInteger(2), UNKNOWN=0, LEADINGDEP=1, NOTLEADING=2, LEADINGNODEP=3, default=0), 0),
    "sample_depends_on" / Default(Enum(BitsInteger(2), UNKNOWN=0, DEPENDS=1, NOTDEPENDS=2, RESERVED=3, default=0), 0),
    "sample_is_depended_on" / Default(Enum(BitsInteger(2), UNKNOWN=0, NOTDISPOSABLE=1, DISPOSABLE=2, RESERVED=3, default=0), 0),
    "sample_has_redundancy" / Default(Enum(BitsInteger(2), UNKNOWN=0, REDUNDANT=1, NOTREDUNDANT=2, RESERVED=3, default=0), 0),
    "sample_padding_value" / Default(BitsInteger(3), 0),
    "sample_is_non_sync_sample" / Default(Flag, False),
    "sample_degradation_priority" / Default(BitsInteger(16), 0),
)

TrackRunBox = Struct(
    "type" / Const(b"trun"),
    "version" / Int8ub,
    "flags" / BitStruct(
        Padding(12),
        "sample_composition_time_offsets_present" / Flag,
        "sample_flags_present" / Flag,
        "sample_size_present" / Flag,
        "sample_duration_present" / Flag,
        Padding(5),
        "first_sample_flags_present" / Flag,
        Padding(1),
        "data_offset_present" / Flag,
    ),
    "sample_count" / Int32ub,
    "data_offset" / Default(If(this.flags.data_offset_present, Int32sb), None),
    "first_sample_flags" / Default(If(this.flags.first_sample_flags_present, Int32ub), None),
    "sample_info" / Array(this.sample_count, Struct(
        "sample_duration" / If(this._.flags.sample_duration_present, Int32ub),
        "sample_size" / If(this._.flags.sample_size_present, Int32ub),
        "sample_flags" / If(this._.flags.sample_flags_present, TrackSampleFlags),
        "sample_composition_time_offsets" / If(
            this._.flags.sample_composition_time_offsets_present,
            IfThenElse(this._.version == 0, Int32ub, Int32sb)
        ),
    ))
)

TrackFragmentHeaderBox = Struct(
    "type" / Const(b"tfhd"),
    "version" / Int8ub,
    "flags" / BitStruct(
        Padding(6),
        "default_base_is_moof" / Flag,
        "duration_is_empty" / Flag,
        Padding(10),
        "default_sample_flags_present" / Flag,
        "default_sample_size_present" / Flag,
        "default_sample_duration_present" / Flag,
        Padding(1),
        "sample_description_index_present" / Flag,
        "base_data_offset_present" / Flag,
    ),
    "track_ID" / Int32ub,
    "base_data_offset" / Default(If(this.flags.base_data_offset_present, Int64ub), None),
    "sample_description_index" / Default(If(this.flags.sample_description_index_present, Int32ub), None),
    "default_sample_duration" / Default(If(this.flags.default_sample_duration_present, Int32ub), None),
    "default_sample_size" / Default(If(this.flags.default_sample_size_present, Int32ub), None),
    "default_sample_flags" / Default(If(this.flags.default_sample_flags_present, TrackSampleFlags), None),
)

MovieExtendsHeaderBox = Struct(
    "type" / Const(b"mehd"),
    "version" / Default(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "fragment_duration" / IfThenElse(this.version == 1,
                                     Default(Int64ub, 0),
                                     Default(Int32ub, 0))
)

TrackExtendsBox = Struct(
    "type" / Const(b"trex"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "track_ID" / Int32ub,
    "default_sample_description_index" / Default(Int32ub, 1),
    "default_sample_duration" / Default(Int32ub, 0),
    "default_sample_size" / Default(Int32ub, 0),
    "default_sample_flags" / Default(TrackSampleFlags, Container()),
)

SegmentIndexBox = Struct(
    "type" / Const(b"sidx"),
    "version" / Int8ub,
    "flags" / Const(Int24ub, 0),
    "reference_ID" / Int32ub,
    "timescale" / Int32ub,
    "earliest_presentation_time" / IfThenElse(this.version == 0, Int32ub, Int64ub),
    "first_offset" / IfThenElse(this.version == 0, Int32ub, Int64ub),
    Padding(2),
    "reference_count" / Int16ub,
    "references" / Array(this.reference_count, BitStruct(
        "reference_type" / Enum(BitsInteger(1), INDEX=1, MEDIA=0),
        "referenced_size" / BitsInteger(31),
        "segment_duration" / BitsInteger(32),
        "starts_with_SAP" / Flag,
        "SAP_type" / BitsInteger(3),
        "SAP_delta_time" / BitsInteger(28),
    ))
)

SampleAuxiliaryInformationSizesBox = Struct(
    "type" / Const(b"saiz"),
    "version" / Const(Int8ub, 0),
    "flags" / BitStruct(
        Padding(23),
        "has_aux_info_type" / Flag,
    ),
    # Optional fields
    "aux_info_type" / Default(If(this.flags.has_aux_info_type, Int32ub), None),
    "aux_info_type_parameter" / Default(If(this.flags.has_aux_info_type, Int32ub), None),
    "default_sample_info_size" / Int8ub,
    "sample_count" / Int32ub,
    # only if sample default_sample_info_size is 0
    "sample_info_sizes" / If(this.default_sample_info_size == 0,
                             Array(this.sample_count, Int8ub))
)

SampleAuxiliaryInformationOffsetsBox = Struct(
    "type" / Const(b"saio"),
    "version" / Int8ub,
    "flags" / BitStruct(
        Padding(23),
        "has_aux_info_type" / Flag,
    ),
    # Optional fields
    "aux_info_type" / Default(If(this.flags.has_aux_info_type, Int32ub), None),
    "aux_info_type_parameter" / Default(If(this.flags.has_aux_info_type, Int32ub), None),
    # Short offsets in version 0, long in version 1
    "offsets" / PrefixedArray(Int32ub, Switch(this.version, {0: Int32ub, 1: Int64ub}))
)

# Movie data box

MovieDataBox = Struct(
    "type" / Const(b"mdat"),
    "data" / GreedyBytes
)

# Media Info Box

SoundMediaHeaderBox = Struct(
    "type" / Const(b"smhd"),
    "version" / Const(Int8ub, 0),
    "flags" / Const(Int24ub, 0),
    "balance" / Default(Int16sb, 0),
    "reserved" / Const(Int16ub, 0)
)


# DASH Boxes

class UUIDBytes(Adapter):
    def _decode(self, obj, context):
        return UUID(bytes=obj)

    def _encode(self, obj, context):
        return obj.bytes


ProtectionSystemHeaderBox = Struct(
    "type" / If(this._.type != b"uuid", Const(b"pssh")),
    "version" / Rebuild(Int8ub, lambda ctx: 1 if (hasattr(ctx, "key_IDs") and ctx.key_IDs) else 0),
    "flags" / Const(Int24ub, 0),
    "system_ID" / UUIDBytes(Bytes(16)),
    "key_IDs" / Default(If(this.version == 1,
                           PrefixedArray(Int32ub, UUIDBytes(Bytes(16)))),
                        None),
    "init_data" / Prefixed(Int32ub, GreedyBytes)
)

TrackEncryptionBox = Struct(
    "type" / If(this._.type != b"uuid", Const(b"tenc")),
    "version" / Default(OneOf(Int8ub, (0, 1)), 0),
    "flags" / Default(Int24ub, 0),
    "_reserved" / Const(Int8ub, 0),
    "default_byte_blocks" / Default(IfThenElse(
        this.version > 0,
        BitStruct(
            # count of encrypted blocks in the protection pattern, where each block is 16-bytes
            "crypt" / Nibble,
            # count of unencrypted blocks in the protection pattern
            "skip" / Nibble
        ),
        Const(Int8ub, 0)
    ), 0),
    "is_encrypted" / OneOf(Int8ub, (0, 1)),
    "iv_size" / OneOf(Int8ub, (0, 8, 16)),
    "key_ID" / UUIDBytes(Bytes(16)),
    "constant_iv" / Default(If(
        this.is_encrypted and this.iv_size == 0,
        PrefixedArray(Int8ub, Byte)
    ), None)
)

SampleEncryptionBox = Struct(
    "type" / If(this._.type != b"uuid", Const(b"senc")),
    "version" / Const(Int8ub, 0),
    "flags" / BitStruct(
        Padding(22),
        "has_subsample_encryption_info" / Flag,
        Padding(1)
    ),
    "sample_encryption_info" / PrefixedArray(Int32ub, Struct(
        "iv" / Bytes(8),
        # include the sub sample encryption information
        "subsample_encryption_info" / Default(If(this.flags.has_subsample_encryption_info, PrefixedArray(Int16ub, Struct(
            "clear_bytes" / Int16ub,
            "cipher_bytes" / Int32ub
        ))), None)
    ))
)

OriginalFormatBox = Struct(
    "type" / Const(b"frma"),
    "original_format" / Default(String(4), b"avc1")
)

SchemeTypeBox = Struct(
    "type" / Const(b"schm"),
    "version" / Default(Int8ub, 0),
    "flags" / Default(Int24ub, 0),
    "scheme_type" / Default(String(4), b"cenc"),
    "scheme_version" / Default(Int32ub, 0x00010000),
    "schema_uri" / Default(If(this.flags & 1 == 1, CString()), None)
)

ProtectionSchemeInformationBox = Struct(
    "type" / Const(b"sinf"),
    # TODO: define which children are required 'schm', 'schi' and 'tenc'
    "children" / LazyBound(lambda _: GreedyRange(Box))
)

# PIFF boxes

UUIDBox = Struct(
    "type" / Const(b"uuid"),
    "extended_type" / UUIDBytes(Bytes(16)),
    "data" / Switch(this.extended_type, {
        UUID("A2394F52-5A9B-4F14-A244-6C427C648DF4"): SampleEncryptionBox,
        UUID("D08A4F18-10F3-4A82-B6C8-32D8ABA183D3"): ProtectionSystemHeaderBox,
        UUID("8974DBCE-7BE7-4C51-84F9-7148F9882554"): TrackEncryptionBox
    }, GreedyBytes)
)

# WebVTT boxes

CueIDBox = Struct(
    "type" / Const(b"iden"),
    "cue_id" / GreedyString("utf8")
)

CueSettingsBox = Struct(
    "type" / Const(b"sttg"),
    "settings" / GreedyString("utf8")
)

CuePayloadBox = Struct(
    "type" / Const(b"payl"),
    "cue_text" / GreedyString("utf8")
)

WebVTTConfigurationBox = Struct(
    "type" / Const(b"vttC"),
    "config" / GreedyString("utf8")
)

WebVTTSourceLabelBox = Struct(
    "type" / Const(b"vlab"),
    "label" / GreedyString("utf8")
)

ContainerBoxLazy = LazyBound(lambda ctx: ContainerBox)


class TellMinusSizeOf(Subconstruct):
    def __init__(self, subcon):
        super(TellMinusSizeOf, self).__init__(subcon)
        self.flagbuildnone = True

    def _parse(self, stream, context, path):
        return stream.tell() - self.subcon.sizeof(context)

    def _build(self, obj, stream, context, path):
        return b""

    def sizeof(self, context=None, **kw):
        return 0


Box = PrefixedIncludingSize(Int32ub, Struct(
    "offset" / TellMinusSizeOf(Int32ub),
    "type" / Peek(String(4, padchar=b" ", paddir="right")),
    Embedded(Switch(this.type, {
        b"ftyp": FileTypeBox,
        b"styp": SegmentTypeBox,
        b"mvhd": MovieHeaderBox,
        b"moov": ContainerBoxLazy,
        b"moof": ContainerBoxLazy,
        b"mfhd": MovieFragmentHeaderBox,
        b"tfdt": TrackFragmentBaseMediaDecodeTimeBox,
        b"trun": TrackRunBox,
        b"tfhd": TrackFragmentHeaderBox,
        b"traf": ContainerBoxLazy,
        b"mvex": ContainerBoxLazy,
        b"mehd": MovieExtendsHeaderBox,
        b"trex": TrackExtendsBox,
        b"trak": ContainerBoxLazy,
        b"mdia": ContainerBoxLazy,
        b"tkhd": TrackHeaderBox,
        b"mdat": MovieDataBox,
        b"free": FreeBox,
        b"skip": SkipBox,
        b"mdhd": MediaHeaderBox,
        b"hdlr": HandlerReferenceBox,
        b"minf": ContainerBoxLazy,
        b"vmhd": VideoMediaHeaderBox,
        b"dinf": ContainerBoxLazy,
        b"dref": DataReferenceBox,
        b"stbl": ContainerBoxLazy,
        b"stsd": SampleDescriptionBox,
        b"stsz": SampleSizeBox,
        b"stz2": SampleSizeBox2,
        b"stts": TimeToSampleBox,
        b"stss": SyncSampleBox,
        b"stsc": SampleToChunkBox,
        b"stco": ChunkOffsetBox,
        b"co64": ChunkLargeOffsetBox,
        b"smhd": SoundMediaHeaderBox,
        b"sidx": SegmentIndexBox,
        b"saiz": SampleAuxiliaryInformationSizesBox,
        b"saio": SampleAuxiliaryInformationOffsetsBox,
        b"btrt": BitRateBox,
        # dash
        b"tenc": TrackEncryptionBox,
        b"pssh": ProtectionSystemHeaderBox,
        b"senc": SampleEncryptionBox,
        b"sinf": ProtectionSchemeInformationBox,
        b"frma": OriginalFormatBox,
        b"schm": SchemeTypeBox,
        b"schi": ContainerBoxLazy,
        # piff
        b"uuid": UUIDBox,
        # HDS boxes
        b'abst': HDSSegmentBox,
        b'asrt': HDSSegmentRunBox,
        b'afrt': HDSFragmentRunBox,
        # WebVTT
        b"vttC": WebVTTConfigurationBox,
        b"vlab": WebVTTSourceLabelBox,
        b"vttc": ContainerBoxLazy,
        b"vttx": ContainerBoxLazy,
        b"iden": CueIDBox,
        b"sttg": CueSettingsBox,
        b"payl": CuePayloadBox
    }, default=RawBox)),
    "end" / Tell
))

ContainerBox = Struct(
    "type" / String(4, padchar=b" ", paddir="right"),
    "children" / GreedyRange(Box)
)

MP4 = GreedyRange(Box)
```

### `wpgskd\vendor\pymp4\util.py`

```python
#!/usr/bin/env python
"""
   Copyright 2016-2019 beardypig
   Copyright 2017-2019 truedread

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
"""
import logging

from pymp4.exceptions import BoxNotFound

log = logging.getLogger(__name__)


class BoxUtil(object):
    @classmethod
    def first(cls, box, type_):
        if box.type == type_:
            return box
        if hasattr(box, "children"):
            for sbox in box.children:
                try:
                    return cls.first(sbox, type_)
                except BoxNotFound:
                    # ignore the except when the box is not found in sub-boxes
                    pass

        raise BoxNotFound("could not find box of type: {}".format(type_))

    @classmethod
    def index(cls, box, type_):
        if hasattr(box, "children"):
            for i, box in enumerate(box.children):
                if box.type == type_:
                    return i

    @classmethod
    def find(cls, box, type_):
        if box.type == type_:
            yield box
        elif hasattr(box, "children"):
            for sbox in box.children:
                for fbox in cls.find(sbox, type_):
                    yield fbox

    @classmethod
    def find_extended(cls, box, extended_type_):
        if hasattr(box, "extended_type"):
            if box.extended_type == extended_type_:
                yield box
            elif hasattr(box, "children"):
                for sbox in box.children:
                    for fbox in cls.find_extended(sbox, extended_type_):
                        yield fbox
        elif hasattr(box, "children"):
            for sbox in box.children:
                for fbox in cls.find_extended(sbox, extended_type_):
                    yield fbox
```

### `wpgskd\vendor\pymp4\tools\__init__.py`

```python
#!/usr/bin/env python
import logging

log = logging.getLogger(__name__)


```

---

## 📊 导出统计

- 成功打包文件数: **113**
- 跳过/失败文件数: **0**

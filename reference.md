# Reference
<details><summary><code>client.<a href="src/MKT_AGI/client.py">create_initial_superadmin</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebPasswordAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create the first superadmin user. Only works when no admin exists.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.create_initial_superadmin(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostSetupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/MKT_AGI/client.py">check_system_setup_status</a>()</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return whether the system has been initialized with a superadmin user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.check_system_setup_status()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## BugReports
<details><summary><code>client.bug_reports.<a href="src/MKT_AGI/bug_reports/client.py">list_all_bug_reports</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalBugreportsInternalDomainBugReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return paginated list of all bug reports. Supports filtering by status and domain label.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bug_reports.list_all_bug_reports()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**status:** `typing.Optional[str]` — Filter by status (pending, reviewed, published, closed)
    
</dd>
</dl>

<dl>
<dd>

**domain:** `typing.Optional[str]` — Filter by domain label (chat, admin, ...)
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Max results (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[int]` — Page offset
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bug_reports.<a href="src/MKT_AGI/bug_reports/client.py">get_bug_report_by_id</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalBugreportsInternalDomainBugReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return full detail of a single bug report including DOM element info and review notes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bug_reports.get_bug_report_by_id(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bug report ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bug_reports.<a href="src/MKT_AGI/bug_reports/client.py">update_bug_report</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalBugreportsInternalDomainBugReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update status and review notes. Status transitions: pending->reviewed, pending->closed, reviewed->published, reviewed->closed, published->closed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bug_reports.update_bug_report(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bug report ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PatchAdminBugReportsIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bug_reports.<a href="src/MKT_AGI/bug_reports/client.py">publish_bug_report_to_git_hub</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a GitHub Issue from a reviewed bug report with structured markdown body and auto-detected domain labels.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bug_reports.publish_bug_report_to_git_hub(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bug report ID (must be in reviewed status)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bug_reports.<a href="src/MKT_AGI/bug_reports/client.py">submit_bug_report</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Submit a bug report with DOM context (element info, viewport). The report is stored with status "pending" for admin review.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bug_reports.submit_bug_report(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostBugReportsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bug_reports.<a href="src/MKT_AGI/bug_reports/client.py">list_my_bug_reports</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalBugreportsInternalDomainBugReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return paginated list of bug reports submitted by the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bug_reports.list_my_bug_reports()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Max results (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[int]` — Page offset
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## AdminBulletins
<details><summary><code>client.admin_bulletins.<a href="src/MKT_AGI/admin_bulletins/client.py">list_all_bulletins_admin</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalBulletinDomainBulletin</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a paginated list of all bulletins including drafts, with optional filters. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_bulletins.list_all_bulletins_admin()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type:** `typing.Optional[str]` — Filter by type
    
</dd>
</dl>

<dl>
<dd>

**category:** `typing.Optional[str]` — Filter by category
    
</dd>
</dl>

<dl>
<dd>

**section:** `typing.Optional[str]` — Filter by section
    
</dd>
</dl>

<dl>
<dd>

**version:** `typing.Optional[str]` — Filter by version
    
</dd>
</dl>

<dl>
<dd>

**include_archived:** `typing.Optional[bool]` — Include archived bulletins
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Max results
    
</dd>
</dl>

<dl>
<dd>

**cursor_val:** `typing.Optional[int]` — Cursor value for pagination
    
</dd>
</dl>

<dl>
<dd>

**cursor_id:** `typing.Optional[int]` — Cursor ID for pagination
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin_bulletins.<a href="src/MKT_AGI/admin_bulletins/client.py">create_a_new_bulletin</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalBulletinDomainBulletin</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new announcement, changelog, or doc. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_bulletins.create_a_new_bulletin(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAdminBulletinsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin_bulletins.<a href="src/MKT_AGI/admin_bulletins/client.py">get_bulletin_by_id_admin</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalBulletinDomainBulletin</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return any bulletin by ID including drafts and expired ones. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_bulletins.get_bulletin_by_id_admin(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bulletin ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin_bulletins.<a href="src/MKT_AGI/admin_bulletins/client.py">update_a_bulletin</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalBulletinDomainBulletin</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing bulletin's content or metadata. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_bulletins.update_a_bulletin(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bulletin ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PutAdminBulletinsIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin_bulletins.<a href="src/MKT_AGI/admin_bulletins/client.py">delete_a_bulletin</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a draft bulletin. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_bulletins.delete_a_bulletin(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bulletin ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin_bulletins.<a href="src/MKT_AGI/admin_bulletins/client.py">archive_a_bulletin</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archive a published or draft bulletin. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_bulletins.archive_a_bulletin(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bulletin ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin_bulletins.<a href="src/MKT_AGI/admin_bulletins/client.py">publish_a_bulletin</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Publish a draft bulletin to make it visible to users. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_bulletins.publish_a_bulletin(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bulletin ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Files
<details><summary><code>client.files.<a href="src/MKT_AGI/files/client.py">list_files_in_directory</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalFilesInternalWebFileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List files in the specified business directory
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.files.list_files_in_directory()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**biz_id:** `typing.Optional[str]` — Business context ID
    
</dd>
</dl>

<dl>
<dd>

**dir_path:** `typing.Optional[str]` — Directory path, defaults to /
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/MKT_AGI/files/client.py">get_file</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalFilesInternalWebFileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get file metadata by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.files.get_file(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — File ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/MKT_AGI/files/client.py">delete_file</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalFilesInternalWebFileDeleteVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a file by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.files.delete_file(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — File ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/MKT_AGI/files/client.py">update_file</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalFilesInternalWebFileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update file name and/or visibility
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.files.update_file(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — File ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PatchAdminFilesIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/MKT_AGI/files/client.py">get_download_url</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalFilesInternalWebFileDownloadVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a presigned download URL for a file
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.files.get_download_url(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — File ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/MKT_AGI/files/client.py">ingest_file_from_url</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalFilesInternalWebFileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Download a file from the given URL and store in the files domain
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.files.ingest_file_from_url(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAdminFilesIngestUrlRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## AdminMarketplace
<details><summary><code>client.admin_marketplace.<a href="src/MKT_AGI/admin_marketplace/client.py">top_resources_ranking_admin</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebTopResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns top models ranked by call count or revenue. Only includes listed/published models.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_marketplace.top_resources_ranking_admin()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sort:** `typing.Optional[str]` — Sort field: calls (default) or revenue
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Max results (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## AdminRevenue
<details><summary><code>client.admin_revenue.<a href="src/MKT_AGI/admin_revenue/client.py">marketplace_fee_revenue_summary</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalPaymentsInternalDomainMarketplaceFeeSummary</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns total marketplace fees, breakdown by resource type and by seller. Requires admin role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin_revenue.marketplace_fee_revenue_summary()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**period:** `typing.Optional[str]` — Period: today, week, all (default all)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Admin
<details><summary><code>client.admin.<a href="src/MKT_AGI/admin/client.py">列出所有系统配置项</a>() -> GithubComMktAgiAixInternalPkgGinxCodeResp</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

返回所有已知配置 key，DB 中有值的显示 DB 值（source=db），无值的显示代码默认值（source=default）
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin.列出所有系统配置项()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin.<a href="src/MKT_AGI/admin/client.py">更新系统配置项</a>(...) -> GithubComMktAgiAixInternalPkgGinxCodeResp</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

更新指定 key 的系统配置值并清除该 key 的缓存
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin.更新系统配置项(
    key="key",
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**key:** `str` — 配置键
    
</dd>
</dl>

<dl>
<dd>

**request:** `PutAdminSysConfigKeyRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.admin.<a href="src/MKT_AGI/admin/client.py">重载系统配置缓存</a>(...) -> GithubComMktAgiAixInternalPkgGinxCodeResp</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

清除指定 key 的内存缓存，下次读取从 DB 加载最新值
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.admin.重载系统配置缓存(
    key="key",
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**key:** `str` — 配置键
    
</dd>
</dl>

<dl>
<dd>

**request:** `typing.Dict[str, typing.Any]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Comments
<details><summary><code>client.comments.<a href="src/MKT_AGI/comments/client.py">list_comments_admin</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalCommentsInternalWebCommentListVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all comments for admin management. Requires session + admin auth.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.comments.list_comments_admin(
    target_type="target_type",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**target_type:** `str` — Target type (article, etc.)
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[str]` — Filter by status (pending, approved, rejected, hidden)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[int]` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/MKT_AGI/comments/client.py">list_comments</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalCommentsInternalWebCommentTreeVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the comment tree for a specific target
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.comments.list_comments(
    target_type="target_type",
    target_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**target_type:** `str` — Target type (article, etc.)
    
</dd>
</dl>

<dl>
<dd>

**target_id:** `int` — Target ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[int]` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/MKT_AGI/comments/client.py">create_comment</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalCommentsInternalDomainComment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new comment or reply. Requires session auth.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.comments.create_comment(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostApiV1CommentsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/MKT_AGI/comments/client.py">update_comment</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalCommentsInternalDomainComment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Edit a comment body. Only the author can edit.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.comments.update_comment(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Comment ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PutApiV1CommentsIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/MKT_AGI/comments/client.py">delete_comment</a>(...) -> GithubComMktAgiAixInternalPkgGinxCodeResp</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Soft-delete a comment. Author or admin can delete.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.comments.delete_comment(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Comment ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Notifications
<details><summary><code>client.notifications.<a href="src/MKT_AGI/notifications/client.py">admin_send_notification</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a notification to a specified user (admin only)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.notifications.admin_send_notification(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostApiV1AdminNotificationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.<a href="src/MKT_AGI/notifications/client.py">list_notifications</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the current user's notifications with cursor-based pagination
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.notifications.list_notifications()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cursor_id:** `typing.Optional[int]` — Cursor ID for pagination
    
</dd>
</dl>

<dl>
<dd>

**cursor_created_at:** `typing.Optional[int]` — Cursor created_at timestamp
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.<a href="src/MKT_AGI/notifications/client.py">mark_notification_as_read</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark a single notification as read for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.notifications.mark_notification_as_read(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Notification ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.<a href="src/MKT_AGI/notifications/client.py">list_preferences</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List notification preferences for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.notifications.list_preferences()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel:** `typing.Optional[str]` — Filter by channel (in_app, email, sms)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.<a href="src/MKT_AGI/notifications/client.py">set_preference</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Set a notification preference for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.notifications.set_preference(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PutApiV1NotificationsPreferencesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.<a href="src/MKT_AGI/notifications/client.py">mark_all_as_read</a>()</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark all notifications as read for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.notifications.mark_all_as_read()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.<a href="src/MKT_AGI/notifications/client.py">get_unread_count</a>()</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the count of unread notifications for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.notifications.get_unread_count()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Payments
<details><summary><code>client.payments.<a href="src/MKT_AGI/payments/client.py">list_payment_orders</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all payment orders for the authenticated user with pagination
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.payments.list_payment_orders()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `typing.Optional[int]` — Page number (default 1)
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="src/MKT_AGI/payments/client.py">create_payment_order</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new top-up payment order with an optional product
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.payments.create_payment_order(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostApiV1PaymentOrdersRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**device_type:** `typing.Optional[str]` — Device type: mobile, tablet, desktop, or unknown
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="src/MKT_AGI/payments/client.py">get_payment_order</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a payment order by ID for the authenticated user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.payments.get_payment_order(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Order ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Wallets
<details><summary><code>client.wallets.<a href="src/MKT_AGI/wallets/client.py">get_transfer_detail</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalPaymentsInternalWebWalletTransferV2Response</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the details of a wallet transfer by transfer number.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wallets.get_transfer_detail(
    transfer_no=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**transfer_no:** `int` — Transfer number
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wallets.<a href="src/MKT_AGI/wallets/client.py">list_wallets</a>() -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalPaymentsInternalWebWalletV2Response</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all wallets for the current authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wallets.list_wallets()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wallets.<a href="src/MKT_AGI/wallets/client.py">get_wallet</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalPaymentsInternalWebWalletV2Response</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single wallet by ID with ownership verification.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wallets.get_wallet(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Wallet ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wallets.<a href="src/MKT_AGI/wallets/client.py">convert_wallet_currency</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Convert all balance from the source wallet to a target-currency wallet in-place, applying the exchange rate with markup. Idempotent via idempotency_key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wallets.convert_wallet_currency(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Source wallet ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostApiV1PaymentWalletsIdConvertCurrencyRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wallets.<a href="src/MKT_AGI/wallets/client.py">list_wallet_transactions</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List paginated transactions for a specific wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wallets.list_wallet_transactions(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Wallet ID
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Page number (default 1)
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Items per page (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wallets.<a href="src/MKT_AGI/wallets/client.py">transfer_between_wallets</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalPaymentsInternalWebWalletTransferEnvelope</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Transfer funds from the source wallet to another wallet belonging to the same user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wallets.transfer_between_wallets(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Source wallet ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostApiV1PaymentWalletsIdTransferRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wallets.<a href="src/MKT_AGI/wallets/client.py">transfer_revenue_wallet_balance_to_main_wallet</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalPaymentsInternalWebWalletTransferEnvelope</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Transfer all balance from a revenue wallet to the user's main wallet. Only revenue wallets are eligible.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wallets.transfer_revenue_wallet_balance_to_main_wallet(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Revenue wallet ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostApiV1PaymentWalletsIdTransferToMainRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Auth
<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">generate_image_captcha</a>() -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebCaptchaGenerateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate a CAPTCHA image and return the token plus base64-encoded PNG.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.generate_image_captcha()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">send_email_verification_code</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a one-time verification code to the given email address. Rate-limited to 1 per 60 seconds.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.send_email_verification_code(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAuthEmailSendRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">verify_email_code_and_authenticate</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Verify the email code and return JWT tokens. Creates a new user account if this email is not registered.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.verify_email_code_and_authenticate(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAuthEmailVerifyRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">exchange_git_hub_code_for_tokens_api</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Exchange a GitHub OAuth authorization code for JWT tokens. Use this from SPAs/mobile apps instead of the web redirect flow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.exchange_git_hub_code_for_tokens_api(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAuthGithubRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">git_hub_o_auth_callback_web</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handle the GitHub OAuth redirect, exchange the code for tokens, and redirect to the frontend.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.git_hub_o_auth_callback_web(
    state="state",
    code="code",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**state:** `str` — OAuth state
    
</dd>
</dl>

<dl>
<dd>

**code:** `str` — GitHub authorization code
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">initiate_git_hub_o_auth</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate an OAuth state and redirect the browser to GitHub's authorization page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.initiate_git_hub_o_auth(
    ref_uri="ref_uri",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**ref_uri:** `str` — Post-auth redirect URI (will be redirected to verbatim)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">exchange_google_code_for_tokens_api</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Exchange a Google OAuth authorization code for JWT tokens. Use this from SPAs/mobile apps instead of the web redirect flow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.exchange_google_code_for_tokens_api(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAuthGoogleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">google_o_auth_callback_web</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handle the Google OAuth redirect, exchange the code for tokens, and redirect to the frontend.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.google_o_auth_callback_web(
    state="state",
    code="code",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**state:** `str` — OAuth state
    
</dd>
</dl>

<dl>
<dd>

**code:** `str` — Google authorization code
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">initiate_google_o_auth</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate an OAuth state and redirect the browser to Google's authorization page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.initiate_google_o_auth(
    ref_uri="ref_uri",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**ref_uri:** `str` — Post-auth redirect URI (will be redirected to verbatim)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">logout_current_user</a>()</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Invalidate all sessions for the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.logout_current_user()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">send_sms_verification_code</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a one-time verification code to the given phone number. Rate-limited to 1 per 60 seconds.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.send_sms_verification_code(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAuthSmsSendRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.<a href="src/MKT_AGI/auth/client.py">verify_sms_code_and_authenticate</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Verify the SMS code and return JWT tokens. Creates a new user account if this phone is not registered.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.auth.verify_sms_code_and_authenticate(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostAuthSmsVerifyRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Bulletins
<details><summary><code>client.bulletins.<a href="src/MKT_AGI/bulletins/client.py">list_published_bulletins</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalBulletinDomainBulletin</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a paginated list of published bulletins with optional filters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bulletins.list_published_bulletins()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type:** `typing.Optional[str]` — Filter by type
    
</dd>
</dl>

<dl>
<dd>

**category:** `typing.Optional[str]` — Filter by category
    
</dd>
</dl>

<dl>
<dd>

**section:** `typing.Optional[str]` — Filter by section
    
</dd>
</dl>

<dl>
<dd>

**version:** `typing.Optional[str]` — Filter by version
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Max results
    
</dd>
</dl>

<dl>
<dd>

**cursor_val:** `typing.Optional[int]` — Cursor value for pagination
    
</dd>
</dl>

<dl>
<dd>

**cursor_id:** `typing.Optional[int]` — Cursor ID for pagination
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bulletins.<a href="src/MKT_AGI/bulletins/client.py">get_bulletin_by_id</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalBulletinDomainBulletin</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a single published bulletin by its ID. Returns 404 if not found or expired.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.bulletins.get_bulletin_by_id(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Bulletin ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Chat
<details><summary><code>client.chat.<a href="src/MKT_AGI/chat/client.py">send_a_chat_completion_request</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Proxies a chat completion to the upstream LLM provider. Supports streaming (SSE) and non-streaming.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.chat.send_a_chat_completion_request(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `typing.Dict[str, typing.Any]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.chat.<a href="src/MKT_AGI/chat/client.py">send_an_anthropic_compatible_message_request</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAnthropicMessageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Adapts Anthropic Messages API requests and responses to the existing AI gateway routing and proxy pipeline.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.chat.send_an_anthropic_compatible_message_request(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.chat.<a href="src/MKT_AGI/chat/client.py">list_available_models</a>() -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all enabled models with extended metadata (name, description, capabilities, default flag).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.chat.list_available_models()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.chat.<a href="src/MKT_AGI/chat/client.py">send_a_responses_api_request</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Adapts OpenAI Responses API requests to Chat Completions. Primarily for Codex CLI compatibility.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.chat.send_a_responses_api_request(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `typing.Dict[str, typing.Any]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## WisdomCommunityPublic
<details><summary><code>client.wisdom_community_public.<a href="src/MKT_AGI/wisdom_community_public/client.py">list_public_communities</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List public communities without authentication. When slug is provided, username is required for joint lookup.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom_community_public.list_public_communities()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**username:** `typing.Optional[str]` — username filter, required when slug is provided
    
</dd>
</dl>

<dl>
<dd>

**slug:** `typing.Optional[str]` — community slug, requires username
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[int]` — pagination offset, default 0
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — pagination limit, default 20, max 100
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## UserGateway
<details><summary><code>client.user_gateway.<a href="src/MKT_AGI/user_gateway/client.py">list_user_models</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalAigatewayInternalDomainModel</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return models owned by the path user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_gateway.list_user_models(
    user_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_gateway.<a href="src/MKT_AGI/user_gateway/client.py">create_user_model</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalAigatewayInternalDomainModel</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a user-owned billable model and bind its primary provider.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_gateway.create_user_model(
    user_id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostGatewayUserIdModelsRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_gateway.<a href="src/MKT_AGI/user_gateway/client.py">get_visible_user_model</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalAigatewayInternalDomainModel</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return one model visible to the path user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_gateway.get_visible_user_model(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_gateway.<a href="src/MKT_AGI/user_gateway/client.py">update_user_model</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalAigatewayInternalDomainModel</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a user-owned billable domain.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_gateway.update_user_model(
    user_id=1,
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PutGatewayUserIdModelsIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_gateway.<a href="src/MKT_AGI/user_gateway/client.py">delete_user_model</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a user-owned model and all its grants.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_gateway.delete_user_model(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_gateway.<a href="src/MKT_AGI/user_gateway/client.py">list_a_model_to_marketplace</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalAigatewayInternalDomainModel</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List a user-owned model to the public marketplace. Requires provider to be enabled, pricing to be set, and a revenue wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_gateway.list_a_model_to_marketplace(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_gateway.<a href="src/MKT_AGI/user_gateway/client.py">unlist_a_model_from_marketplace</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalAigatewayInternalDomainModel</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unlist a user-owned model from the public marketplace (visibility = private).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_gateway.unlist_a_model_from_marketplace(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## UserModels
<details><summary><code>client.user_models.<a href="src/MKT_AGI/user_models/client.py">list_model_visibility_filters</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayUint</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return all users who have filter access to a model
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_models.list_model_visibility_filters(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_models.<a href="src/MKT_AGI/user_models/client.py">add_model_visibility_filter</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Grant a user access to a private model via filter
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_models.add_model_visibility_filter(
    user_id=1,
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostGatewayUserIdModelsIdFiltersRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_models.<a href="src/MKT_AGI/user_models/client.py">remove_model_visibility_filter</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke a user's access to a filtered model
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_models.remove_model_visibility_filter(
    user_id=1,
    id=1,
    target_user_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Model ID
    
</dd>
</dl>

<dl>
<dd>

**target_user_id:** `int` — Target user ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## UserProviders
<details><summary><code>client.user_providers.<a href="src/MKT_AGI/user_providers/client.py">list_visible_providers</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalAigatewayInternalWebUserProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return user-owned and global providers with masked API keys.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_providers.list_visible_providers(
    user_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_providers.<a href="src/MKT_AGI/user_providers/client.py">create_user_provider</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebUserProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a user-owned LLM provider with encrypted API service.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_providers.create_user_provider(
    user_id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostGatewayUserIdProvidersRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_providers.<a href="src/MKT_AGI/user_providers/client.py">get_visible_provider</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebUserProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return one visible provider with masked API service.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_providers.get_visible_provider(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Provider ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_providers.<a href="src/MKT_AGI/user_providers/client.py">update_user_provider</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebUserProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a user-owned provider. Global providers cannot be modified.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_providers.update_user_provider(
    user_id=1,
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Provider ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PutGatewayUserIdProvidersIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_providers.<a href="src/MKT_AGI/user_providers/client.py">delete_user_provider</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a user-owned provider if no user models reference it.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_providers.delete_user_provider(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Provider ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_providers.<a href="src/MKT_AGI/user_providers/client.py">test_existing_provider</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebTestProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Test an existing provider's connectivity and re-discover available models.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_providers.test_existing_provider(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Provider ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_providers.<a href="src/MKT_AGI/user_providers/client.py">test_provider_connection</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebTestProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Test provider connectivity and list available models, before creating a provider record.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_providers.test_provider_connection(
    user_id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostGatewayUserIdProvidersTestRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## UserRoutes
<details><summary><code>client.user_routes.<a href="src/MKT_AGI/user_routes/client.py">list_user_model_routes</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalAigatewayInternalWebUserRouteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return all routes for the authenticated user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_routes.list_user_model_routes(
    user_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_routes.<a href="src/MKT_AGI/user_routes/client.py">create_user_model_route</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebUserRouteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a user-scoped model_prefix → provider routing override.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_routes.create_user_model_route(
    user_id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostGatewayUserIdRoutesRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_routes.<a href="src/MKT_AGI/user_routes/client.py">get_user_model_route</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebUserRouteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a single route by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_routes.get_user_model_route(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Route ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_routes.<a href="src/MKT_AGI/user_routes/client.py">delete_user_model_route</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a user route by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_routes.delete_user_model_route(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Route ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_routes.<a href="src/MKT_AGI/user_routes/client.py">list_route_visibility_filters</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayUint</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return all users who have filter access to a route
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_routes.list_route_visibility_filters(
    user_id=1,
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Route ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_routes.<a href="src/MKT_AGI/user_routes/client.py">add_route_visibility_filter</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Grant a user access to a route via filter
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_routes.add_route_visibility_filter(
    user_id=1,
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Route ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostGatewayUserIdRoutesIdFiltersRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_routes.<a href="src/MKT_AGI/user_routes/client.py">remove_route_visibility_filter</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke a user's access to a filtered route
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_routes.remove_route_visibility_filter(
    user_id=1,
    id=1,
    target_user_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**id:** `int` — Route ID
    
</dd>
</dl>

<dl>
<dd>

**target_user_id:** `int` — Target user ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Gateway
<details><summary><code>client.gateway.<a href="src/MKT_AGI/gateway/client.py">test_model_connectivity</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebTestModelResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sends a "say hi" prompt to the specified provider+model and returns the response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.gateway.test_model_connectivity(
    user_id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID or username
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostGatewayUserIdTestModelRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.gateway.<a href="src/MKT_AGI/gateway/client.py">list_request_logs</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebListLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns paginated request logs for the current user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.gateway.list_request_logs()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model_id:** `typing.Optional[int]` — Filter by model ID
    
</dd>
</dl>

<dl>
<dd>

**provider_id:** `typing.Optional[int]` — Filter by provider ID
    
</dd>
</dl>

<dl>
<dd>

**session_id:** `typing.Optional[int]` — Filter by session ID
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[int]` — Filter by HTTP status code
    
</dd>
</dl>

<dl>
<dd>

**stream:** `typing.Optional[bool]` — Filter by stream (true/false)
    
</dd>
</dl>

<dl>
<dd>

**date_from:** `typing.Optional[str]` — Start date (YYYY-MM-DD)
    
</dd>
</dl>

<dl>
<dd>

**date_to:** `typing.Optional[str]` — End date (YYYY-MM-DD)
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[str]` — Sort field: created_at, latency_ms, cost, total_tokens
    
</dd>
</dl>

<dl>
<dd>

**order:** `typing.Optional[str]` — Sort order: asc, desc (default desc)
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[int]` — Pagination offset (default 0)
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.gateway.<a href="src/MKT_AGI/gateway/client.py">list_models_visible_to_current_principal</a>() -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns models that the current authenticated user (via cookie or API key) is allowed to see.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.gateway.list_models_visible_to_current_principal()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.gateway.<a href="src/MKT_AGI/gateway/client.py">seller_revenue_summary</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebSellerRevenueResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns revenue summary for all models owned by the current user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.gateway.seller_revenue_summary()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**period:** `typing.Optional[str]` — Period: today, week, all (default all)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.gateway.<a href="src/MKT_AGI/gateway/client.py">list_usage_records</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebListUsageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns paginated daily usage records for the current user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.gateway.list_usage_records()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model_id:** `typing.Optional[int]` — Filter by model ID
    
</dd>
</dl>

<dl>
<dd>

**date_from:** `typing.Optional[str]` — Start date (YYYY-MM-DD)
    
</dd>
</dl>

<dl>
<dd>

**date_to:** `typing.Optional[str]` — End date (YYYY-MM-DD)
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[str]` — Sort field: record_date, call_count, total_cost
    
</dd>
</dl>

<dl>
<dd>

**order:** `typing.Optional[str]` — Sort order: asc, desc (default desc)
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[int]` — Pagination offset (default 0)
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Sessions
<details><summary><code>client.sessions.<a href="src/MKT_AGI/sessions/client.py">list_ai_sessions</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalAigatewayInternalDomainAiSession</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return paginated list of AI chat sessions for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.sessions.list_ai_sessions()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sessions.<a href="src/MKT_AGI/sessions/client.py">create_ai_session</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalAigatewayInternalDomainAiSession</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new AI chat session for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.sessions.create_ai_session(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostGatewaySessionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sessions.<a href="src/MKT_AGI/sessions/client.py">delete_ai_session</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Soft-delete an AI chat session
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.sessions.delete_ai_session(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Session ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sessions.<a href="src/MKT_AGI/sessions/client.py">update_ai_session</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultAny</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update session title or metadata
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.sessions.update_ai_session(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Session ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PatchGatewaySessionsIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Iam
<details><summary><code>client.iam.<a href="src/MKT_AGI/iam/client.py">list_api_keys</a>() -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalIamInternalWebApiKeyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List API key metadata for the authenticated user. Raw keys and hashes are never returned.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.iam.list_api_keys()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.iam.<a href="src/MKT_AGI/iam/client.py">create_api_key</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalIamInternalWebCreateApiKeyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an API key for the authenticated user. The raw API key is returned only once in this response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.iam.create_api_key(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostIamApiKeysRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.iam.<a href="src/MKT_AGI/iam/client.py">revoke_api_key</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke an API key owned by the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.iam.revoke_api_key(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.iam.<a href="src/MKT_AGI/iam/client.py">list_visibility_filters</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayUint</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

列出资源的可见性过滤器用户列表。返回被添加到可见性白名单中的用户 ID。
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.iam.list_visibility_filters(
    resource_type="resource_type",
    resource_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resource_type:** `str` — Resource type
    
</dd>
</dl>

<dl>
<dd>

**resource_id:** `int` — Resource ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.iam.<a href="src/MKT_AGI/iam/client.py">add_visibility_filter</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

添加可见性过滤器，将指定用户添加到资源的可见性白名单中。
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.iam.add_visibility_filter(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostIamVisibilityFiltersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.iam.<a href="src/MKT_AGI/iam/client.py">remove_visibility_filter</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

移除可见性过滤器，将指定用户从资源的可见性白名单中移除。
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.iam.remove_visibility_filter(
    resource_type="resource_type",
    resource_id=1,
    user_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resource_type:** `str` — Resource type
    
</dd>
</dl>

<dl>
<dd>

**resource_id:** `int` — Resource ID
    
</dd>
</dl>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Marketplace
<details><summary><code>client.marketplace.<a href="src/MKT_AGI/marketplace/client.py">list_marketplace_models</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAigatewayInternalWebMarketplaceListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns paginated marketplace models with search, price filter, and sort.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.marketplace.list_marketplace_models()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**search:** `typing.Optional[str]` — Search by name or description
    
</dd>
</dl>

<dl>
<dd>

**min_price:** `typing.Optional[float]` — Minimum output price filter
    
</dd>
</dl>

<dl>
<dd>

**max_price:** `typing.Optional[float]` — Maximum output price filter
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[str]` — Sort field: listed_at, call_count, output_price (default listed_at)
    
</dd>
</dl>

<dl>
<dd>

**order:** `typing.Optional[str]` — Sort order: asc, desc (default desc)
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Page number (default 1)
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Conversations
<details><summary><code>client.conversations.<a href="src/MKT_AGI/conversations/client.py">list_conversations</a>() -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalMessagingInternalDomainConversationSummary</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List conversations for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.conversations.list_conversations()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="src/MKT_AGI/conversations/client.py">create_conversation</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalMessagingInternalDomainConversation</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new conversation with participants
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.conversations.create_conversation(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostMessagingConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="src/MKT_AGI/conversations/client.py">get_conversation</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalMessagingInternalDomainConversation</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a conversation by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.conversations.get_conversation(
    conv_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**conv_id:** `int` — Conversation ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="src/MKT_AGI/conversations/client.py">add_participant</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a user to a conversation
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.conversations.add_participant(
    conv_id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**conv_id:** `int` — Conversation ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostMessagingConversationsConvIdParticipantsRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Messages
<details><summary><code>client.messages.<a href="src/MKT_AGI/messages/client.py">get_messages</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayGithubComMktAgiAixInternalMessagingInternalDomainMessage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve messages in a conversation
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.messages.get_messages(
    conv_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**conv_id:** `int` — Conversation ID
    
</dd>
</dl>

<dl>
<dd>

**after_seq:** `typing.Optional[int]` — Only messages after this sequence number
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page limit (default 20, max 100)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/MKT_AGI/messages/client.py">send_message</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultGithubComMktAgiAixInternalMessagingInternalDomainMessage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a message in a conversation
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.messages.send_message(
    conv_id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**conv_id:** `int` — Conversation ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostMessagingConversationsConvIdMessagesRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/MKT_AGI/messages/client.py">mark_messages_as_read</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark messages as read up to the given sequence number
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.messages.mark_messages_as_read(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostMessagingReadRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Devices
<details><summary><code>client.devices.<a href="src/MKT_AGI/devices/client.py">register_device</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Register a push notification device for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.devices.register_device(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostMessagingDevicesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.devices.<a href="src/MKT_AGI/devices/client.py">unregister_device</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unregister a push notification device
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.devices.unregister_device(
    device_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**device_id:** `int` — Device ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## WisdomPublic
<details><summary><code>client.wisdom_public.<a href="src/MKT_AGI/wisdom_public/client.py">list_public_contents</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List public content nodes without authentication
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom_public.list_public_contents()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**username:** `typing.Optional[str]` — filter by author username (resolved to user_id by middleware)
    
</dd>
</dl>

<dl>
<dd>

**kind:** `typing.Optional[str]` — kind filter
    
</dd>
</dl>

<dl>
<dd>

**type:** `typing.Optional[str]` — type filter
    
</dd>
</dl>

<dl>
<dd>

**community_id:** `typing.Optional[int]` — community ID filter
    
</dd>
</dl>

<dl>
<dd>

**community_slug:** `typing.Optional[str]` — community slug filter, requires username
    
</dd>
</dl>

<dl>
<dd>

**slug:** `typing.Optional[str]` — slug filter, scoped within community_slug when present
    
</dd>
</dl>

<dl>
<dd>

**promise_search:** `typing.Optional[str]` — search by promise keyword
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[int]` — pagination offset, default 0
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — pagination limit, default 20, max 100
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## UserSecrets
<details><summary><code>client.user_secrets.<a href="src/MKT_AGI/user_secrets/client.py">list_user_secrets</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalAccountsInternalWebUserSecretResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List metadata for all secrets owned by the specified user. Secret values are never returned by this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_secrets.list_user_secrets(
    user_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_secrets.<a href="src/MKT_AGI/user_secrets/client.py">get_user_secret</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebUserSecretValueResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return one decrypted secret value for the specified user and service.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_secrets.get_user_secret(
    user_id=1,
    key="key",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**key:** `str` — Secret key
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_secrets.<a href="src/MKT_AGI/user_secrets/client.py">create_or_update_user_secret</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebUserSecretResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Encrypt and store a secret value for the specified user and service. The response does not include the secret value.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_secrets.create_or_update_user_secret(
    user_id=1,
    key="key",
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**key:** `str` — Secret key
    
</dd>
</dl>

<dl>
<dd>

**request:** `PutSecretsUserIdKeyRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user_secrets.<a href="src/MKT_AGI/user_secrets/client.py">delete_user_secret</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebDeleteUserSecretResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete one secret by user ID and service.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user_secrets.delete_user_secret(
    user_id=1,
    key="key",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `int` — User ID
    
</dd>
</dl>

<dl>
<dd>

**key:** `str` — Secret key
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## User
<details><summary><code>client.user.<a href="src/MKT_AGI/user/client.py">get_current_user_profile</a>() -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the authenticated user's profile information.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user.get_current_user_profile()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/MKT_AGI/user/client.py">update_current_user_profile</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the authenticated user's name and/or avatar_url. Name must be unique.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user.update_current_user_profile(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PatchUserMeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/MKT_AGI/user/client.py">get_presigned_avatar_upload_url</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebAvatarUploadUrlResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate a presigned S3 URL for direct browser avatar upload. Content type must be image/png, image/jpeg, or image/webp. Max size 5MB.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user.get_presigned_avatar_upload_url(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostUserMeAvatarUploadUrlRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/MKT_AGI/user/client.py">confirm_and_soft_delete_the_account</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Verify the deletion code, snapshot original contacts, NULL the login identifiers, kill all sessions, and clear the session cookie.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user.confirm_and_soft_delete_the_account(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostUserMeDeletionConfirmRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/MKT_AGI/user/client.py">send_account_deletion_confirmation_code</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a 6-digit confirmation code to the user's bound email (or phone if no email) to confirm account deletion.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user.send_account_deletion_confirmation_code(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `typing.Dict[str, typing.Any]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/MKT_AGI/user/client.py">switch_current_session_user</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalAccountsInternalWebUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Switch the session's current effective user to the session owner or one direct sub-user of the owner.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user.switch_current_session_user(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostUserSwitchRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/MKT_AGI/user/client.py">list_switchable_users</a>() -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalAccountsInternalWebUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the session owner plus all direct sub-users that the current session can switch to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.user.list_switchable_users()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Accounts
<details><summary><code>client.accounts.<a href="src/MKT_AGI/accounts/client.py">receive_git_hub_webhook_events</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handle incoming GitHub webhook events (installation, push, etc.)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.accounts.receive_git_hub_webhook_events(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `typing.Dict[str, typing.Any]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Wisdom
<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">list_contents</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List content nodes with optional filters (kind, type, community_id, etc.)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.list_contents()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**kind:** `typing.Optional[str]` — kind filter
    
</dd>
</dl>

<dl>
<dd>

**type:** `typing.Optional[str]` — type filter
    
</dd>
</dl>

<dl>
<dd>

**community_id:** `typing.Optional[int]` — community ID filter
    
</dd>
</dl>

<dl>
<dd>

**min_confidence:** `typing.Optional[float]` — minimum confidence filter
    
</dd>
</dl>

<dl>
<dd>

**promise_search:** `typing.Optional[str]` — search by promise keyword
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[int]` — pagination offset, default 0
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — pagination limit, default 20, max 100
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">create_content</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebWisdomResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new content node in the property graph
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.create_content(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostWisdomRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">get_content</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebWisdomWithContextResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a content node by ID with optional depth context (0 or 1)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.get_content(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Content ID
    
</dd>
</dl>

<dl>
<dd>

**depth:** `typing.Optional[int]` — Context depth: 0 (default) or 1
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">delete_content</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebWisdomDeleteVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a content node by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.delete_content(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Content ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">update_content</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebWisdomResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a content node's fields with optimistic locking via version
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.update_content(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Content ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PatchWisdomIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">get_content_logs</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultArrayInternalWisdomInternalWebLogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get audit log entries for a specific content node
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.get_content_logs(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Content ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">add_relation</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebRelationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a directed relation edge from source content to target content
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.add_relation(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Source content ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PostWisdomIdRelationsRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">remove_relation</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebWisdomDeleteVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a relation edge by relation ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.remove_relation(
    id=1,
    rid=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Source content ID
    
</dd>
</dl>

<dl>
<dd>

**rid:** `int` — Relation ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">cluster_contents</a>() -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebTriggerStatusVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Trigger community detection clustering on user's content graph
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.cluster_contents()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom.<a href="src/MKT_AGI/wisdom/client.py">get_subgraph</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebGraphResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the content subgraph for a specific community
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom.get_subgraph(
    community_id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**community_id:** `int` — Community ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## WisdomCommunity
<details><summary><code>client.wisdom_community.<a href="src/MKT_AGI/wisdom_community/client.py">list_communities</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List communities for the current user with pagination
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom_community.list_communities()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**offset:** `typing.Optional[int]` — pagination offset, default 0
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — pagination limit, default 20, max 100
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom_community.<a href="src/MKT_AGI/wisdom_community/client.py">create_community</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebCommunityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new community
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom_community.create_community(
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PostWisdomCommunityRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom_community.<a href="src/MKT_AGI/wisdom_community/client.py">get_community</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebCommunityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a community by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom_community.get_community(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Community ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom_community.<a href="src/MKT_AGI/wisdom_community/client.py">delete_community</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebWisdomDeleteVo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a community and disassociate its wisdoms
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom_community.delete_community(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Community ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.wisdom_community.<a href="src/MKT_AGI/wisdom_community/client.py">update_community</a>(...) -> GithubComMktAgiAixInternalPkgGinxResultInternalWisdomInternalWebCommunityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a community's fields
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from MKT_AGI import MktAgiApi
from MKT_AGI.environment import MktAgiApiEnvironment

client = MktAgiApi(
    api_key="<value>",
    environment=MktAgiApiEnvironment.DEFAULT,
)

client.wisdom_community.update_community(
    id=1,
    request={
        "key": "value"
    },
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` — Community ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `PatchWisdomCommunityIdRequestBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>


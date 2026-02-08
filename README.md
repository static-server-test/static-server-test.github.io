# Static Server Test

## Description

This project is a set of HTML pages which can be deployed to a static server (eg. GitHub Pages, etc.) to test how is serves files, folders and deals with trailing slashes.

## How does it work?

Deploy the `docs` folder to your favorite static site server and then navigate to the root path of your deployment where a script will generate a report. Below are reports for a few popular services.

Additionally you can run this locally using your favorite static server. For example run `npx serve docs` and navigate to http://localhost:3000 to view the report.

## Reports

Below are reports from some populare static servers and services

### `npx serve`

No configuration

|Path|Expected|Actual|Pass|Status|Location|
|---|---|---|---|---|---|
|/file|file.html|file.html|✅|200|http://localhost:3000/file|
|/file/|file.html|file.html|✅|200|http://localhost:3000/file/|
|/file.html|file.html|file.html|✅|➡️|http://localhost:3000/file|
|/folder|folder/index.html|folder/index.html|✅|200|http://localhost:3000/folder|
|/folder/|folder/index.html|folder/index.html|✅|200|http://localhost:3000/folder/|
|/folder/index.html|folder/index.html|folder/index.html|✅|➡️|http://localhost:3000/folder|
|/both|both.html|both/index.html|❌|200|http://localhost:3000/both|
|/both/|both/index.html|both/index.html|✅|200|http://localhost:3000/both/|
|/both.html|both.html|both/index.html|❌|➡️|http://localhost:3000/both|
|/both/index.html|both/index.html|both/index.html|✅|➡️|http://localhost:3000/both|
|/group|group.html|group.html|✅|200|http://localhost:3000/group|
|/group/|group.html|group.html|✅|200|http://localhost:3000/group/|
|/group.html|group.html|group.html|✅|➡️|http://localhost:3000/group|


### GitHub Pages

https://static-server-test.github.io/

|Path|Expected|Actual|Pass|Status|Location|
|---|---|---|---|---|---|
|/file|file.html|file.html|✅|200|https://static-server-test.github.io/file|
|/file/|file.html||❌|404|https://static-server-test.github.io/file/|
|/file.html|file.html|file.html|✅|200|https://static-server-test.github.io/file.html|
|/folder|folder/index.html|folder/index.html|✅|➡️|https://static-server-test.github.io/folder/|
|/folder/|folder/index.html|folder/index.html|✅|200|https://static-server-test.github.io/folder/|
|/folder/index.html|folder/index.html|folder/index.html|✅|200|https://static-server-test.github.io/folder/index.html|
|/both|both.html|both.html|✅|200|https://static-server-test.github.io/both|
|/both/|both/index.html|both/index.html|✅|200|https://static-server-test.github.io/both/|
|/both.html|both.html|both.html|✅|200|https://static-server-test.github.io/both.html|
|/both/index.html|both/index.html|both/index.html|✅|200|https://static-server-test.github.io/both/index.html|
|/group|group.html|group.html|✅|200|https://static-server-test.github.io/group|
|/group/|group.html||❌|404|https://static-server-test.github.io/group/|
|/group.html|group.html|group.html|✅|200|https://static-server-test.github.io/group.html|

### Cloudflare Pages

https://static-server-test.rturnq.workers.dev/

|Path|Expected|Actual|Pass|Status|Location|
|---|---|---|---|---|---|
|/file|file.html|file.html|✅|200|https://static-server-test.rturnq.workers.dev/file|
|/file/|file.html|file.html|✅|➡️|https://static-server-test.rturnq.workers.dev/file|
|/file.html|file.html|file.html|✅|➡️|https://static-server-test.rturnq.workers.dev/file|
|/folder|folder/index.html|folder/index.html|✅|➡️|https://static-server-test.rturnq.workers.dev/folder/|
|/folder/|folder/index.html|folder/index.html|✅|200|https://static-server-test.rturnq.workers.dev/folder/|
|/folder/index.html|folder/index.html|folder/index.html|✅|➡️|https://static-server-test.rturnq.workers.dev/folder/|
|/both|both.html|both.html|✅|200|https://static-server-test.rturnq.workers.dev/both|
|/both/|both/index.html|both/index.html|✅|200|https://static-server-test.rturnq.workers.dev/both/|
|/both.html|both.html|both.html|✅|➡️|https://static-server-test.rturnq.workers.dev/both|
|/both/index.html|both/index.html|both/index.html|✅|➡️|https://static-server-test.rturnq.workers.dev/both/|
|/group|group.html|group.html|✅|200|https://static-server-test.rturnq.workers.dev/group|
|/group/|group.html|group.html|✅|➡️|https://static-server-test.rturnq.workers.dev/group|
|/group.html|group.html|group.html|✅|➡️|https://static-server-test.rturnq.workers.dev/group|
<!-- Copyright 2013 - 2018 Software AG, Darmstadt, Germany and/or its licensors

   SPDX-License-Identifier: Apache-2.0

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
     WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
     See the License for the specific language governing permissions and

     limitations under the License.                                                  

-->
# Command Central Internal GA Product and Fix Repositories

Use this template to create internal GA Software AG product and fix repositories in Command Central that replicate the production repositories, provided to Software AG customers.

## Requirements

### Supported Software AG releases

* Command Central 10.1 and higher

### Supported platforms

All supported Windows and UNIX platforms.

## Running as a standalone composite template

To create a internal GA Software AG product and fix repositories in Command Central:

```bash
sagcc exec templates composite apply sag-cc-repos-ga --sync-job --wait 360
```

> IMPORTANT: If you use Command Central 10.1 you have to monitor the job completion with a separate command, instead of the `--sync-job` option:

```bash
sagcc list jobmanager jobs <jobIdFromAboveCommand> --wait 360 -e DONE
```
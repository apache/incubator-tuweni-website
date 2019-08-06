---
layout: page
title: Downloads
description: Apache Tuweni Downloads page
group: nav-right
---
<!--
{% comment %}
Licensed to the Apache Software Foundation (ASF) under one or more
contributor license agreements.  See the NOTICE file distributed with
this work for additional information regarding copyright ownership.
The ASF licenses this file to you under the Apache License, Version 2.0
(the "License"); you may not use this file except in compliance with
the License.  You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
{% endcomment %}
-->
{% include JB/setup %}

## {{ site.data.project.name }} Downloads

{{ site.data.project.name }} is made available as a distribution and through Maven Central.

### Release Artifacts

<table class="table table-hover sortable">
    <thead>
        <tr>
            <th><b>Name</b></th>
            <th><b>Archive</b></th>
            <th><b>SHA-512</b></th>
            <th><b>Signature</b></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (tgz)</td>
            <td><a href="https://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-bin-{{site.data.project.latest_release}}-incubating.tgz">tgz</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-bin-{{site.data.project.latest_release}}-incubating.tgz.sha512">SHA-512</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-bin-{{site.data.project.latest_release}}-incubating.tgz.asc">ASC</a></td>
        </tr>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (zip)</td>
            <td><a href="http://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-bin-{{site.data.project.latest_release}}-incubating.zip">zip</a></td>
            <td><a href="http://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-bin-{{site.data.project.latest_release}}-incubating.zip.sha512">SHA-512</a></td>
            <td><a href="http://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-bin-{{site.data.project.latest_release}}-incubating.zip.asc">ASC</a></td>
        </tr>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (source tgz)</td>
            <td><a href="https://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-src-{{site.data.project.latest_release}}-incubating.tgz">tgz</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-src-{{site.data.project.latest_release}}-incubating.tgz.sha512">SHA-512</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-src-{{site.data.project.latest_release}}-incubating.tgz.asc">ASC</a></td>
        </tr>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (source zip)</td>
            <td><a href="https://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-src-{{site.data.project.latest_release}}-incubating.zip">zip</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-src-{{site.data.project.latest_release}}-incubating.zip.sha512">SHA-512</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-src-{{site.data.project.latest_release}}-incubating.zip.asc">ASC</a></td>
        </tr>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (Gossip application tgz)</td>
            <td><a href="https://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-gossip-{{site.data.project.latest_release}}-incubating.tgz">tgz</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-gossip-{{site.data.project.latest_release}}-incubating.tgz.sha512">SHA-512</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-gossip-{{site.data.project.latest_release}}-incubating.tgz.asc">ASC</a></td>
        </tr>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (Gossip application zip)</td>
            <td><a href="https://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-gossip-{{site.data.project.latest_release}}-incubating.zip">zip</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-gossip-{{site.data.project.latest_release}}-incubating.zip.sha512">SHA-512</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-gossip-{{site.data.project.latest_release}}-incubating.zip.asc">ASC</a></td>
        </tr>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (Relayer application tgz)</td>
            <td><a href="https://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-relayer-{{site.data.project.latest_release}}-incubating.tgz">tgz</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-relayer-{{site.data.project.latest_release}}-incubating.tgz.sha512">SHA-512</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-relayer-{{site.data.project.latest_release}}-incubating.tgz.asc">ASC</a></td>
        </tr>
        <tr>
            <td>{{ site.data.project.name }} {{site.data.project.latest_release}} (Relayer application zip)</td>
            <td><a href="https://www.apache.org/dyn/closer.lua/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-relayer-{{site.data.project.latest_release}}-incubating.zip">zip</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-relayer-{{site.data.project.latest_release}}-incubating.zip.sha512">SHA-512</a></td>
            <td><a href="https://www.apache.org/dist/{{site.data.project.incubator_slash_name}}/{{site.data.project.latest_release}}-incubating/{{site.data.project.unix_name}}-relayer-{{site.data.project.latest_release}}-incubating.zip.asc">ASC</a></td>
        </tr>
        <!--tr>
            <td>Release Notes</td>
            <td><a href="/releases/spark/{{ site.data.project.latest_release }}/release-notes">{{ site.data.project.latest_release }}</a></td>
            <td></td>
            <td></td>
            <td></td>
        </tr-->
    </tbody>
</table>

Choose a source distribution in either *tar* or *zip* format,
and [verify](https://www.apache.org/dyn/closer.cgi#verify)
using the corresponding *pgp* signature (using the committer file in
[KEYS](https://www.apache.org/dist/{{ site.data.project.incubator_slash_name }}/KEYS)).
If you cannot do that, the *md5* hash file may be used to check that the
download has completed OK.

For fast downloads, current source distributions are hosted on mirror servers;
older source distributions are in the
[archive](https://archive.apache.org/dist/{{ site.data.project.incubator_slash_name }}/).
If a download from a mirror fails, retry, and the second download will likely
succeed.

For security, hash and signature files are always hosted at
[Apache](https://www.apache.org/dist).

### Maven Central

You can download Apache Tuweni dependencies through Maven Central.

*We are still in the process of publishing our bits to Maven Central and will update this page once it is completed.*
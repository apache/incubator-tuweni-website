---
layout: page
title: Apache Tuweni | Community
description: Project Community Page
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

<br/><br/><br/>

## {{ site.data.project.name }} Community

Every volunteer project obtains its strength from the people involved in it. We invite you to participate as much or as little as you choose.

You can:

* Use our project and provide a feedback.
* Provide us with the use-cases.
* Report bugs and submit patches.
* Contribute code, javadocs, documentation.

### Mailing list

Get help using {{ site.data.project.short_name }} or contribute to the project on our mailing lists:

{% if site.data.project.user_list %}
* [{{ site.data.project.user_list }}](mailto:{{ site.data.project.user_list }}) is for usage questions, help, and announcements. [subscribe](mailto:{{ site.data.project.user_list_subscribe }}?subject=send this email to subscribe),     [unsubscribe](mailto:{{ site.data.project.dev_list_unsubscribe }}?subject=send this email to unsubscribe), [archives]({{ site.data.project.user_list_archive_mailarchive }})
{% endif %}
* [{{ site.data.project.dev_list }}](mailto:{{ site.data.project.dev_list }}) is for people who want to contribute code to {{ site.data.project.short_name }}. [subscribe](mailto:{{ site.data.project.dev_list_subscribe }}?subject=send this email to subscribe), [unsubscribe](mailto:{{ site.data.project.dev_list_unsubscribe }}?subject=send this email to unsubscribe), [archives]({{ site.data.project.dev_list_archive_mailarchive }})
* [{{ site.data.project.commits_list }}](mailto:{{ site.data.project.commits_list }}) is for commit messages and patches to {{ site.data.project.short_name }}. [subscribe](mailto:{{ site.data.project.commits_list_subscribe }}?subject=send this email to subscribe), [unsubscribe](mailto:{{ site.data.project.commits_list_unsubscribe }}?subject=send this email to unsubscribe), [archives]({{ site.data.project.commits_list_archive_mailarchive }})


### Issue tracker

We use <a href="https://github.com/apache/incubator-tuweni/issues">Github for bug reports and feature requests</a>, with <span id="open">(loading)</span> issues.

<div>
  <table class="table table-bordered table-hover">
    <thead>
      <tr>
      <th  style="min-width:50px">
        #
      </th>
      <th>
        Title
      </th>
      </tr>
    </thead>
    <tbody id="github-issues">
    </tbody>
  </table>
</div>

<script>
    var urlToGetAllOpenBugs = "https://api.github.com/repos/apache/incubator-tuweni/issues?state=open";

    $(document).ready(function () {
        $.getJSON(urlToGetAllOpenBugs, function (allIssues) {
            $("span#open").text(allIssues.length);
            $.each(allIssues, function (i, issue) {

                $("tbody#github-issues")
                    .append("<tr><td><a href=\"" + issue.html_url + "\"><strong>#" + issue.number + "</strong></a></td><td><a href=\"" + issue.html_url + "\">" + issue.title + "</a></td></tr>");
            });
        });
    });
</script>

### Source Code

The project sources are accessible via the [source code repository]({{ site.data.project.source_repository }}) which is also mirrored at [Apache]({{ site.data.project.source_repository_mirror }}).

### Website Source Code

The project website sources are accessible via the [website source code repository]({{ site.data.project.website_repository }}) which is also mirrored at [Apache]({{ site.data.project.website_repository_mirror }}).

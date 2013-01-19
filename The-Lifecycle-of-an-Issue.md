## Overview

The [Spring Framework JIRA](https://jira.springsource.org/browse/SPR) has many issues. To ensure every issue is given attention, we use a process. Understanding that process will set your expectations and enable you to interpret the state an issue is currently in regardless of when it was created, a couple of days or a couple of years ago. 

The process described here has been followed for issues created since January 2011. We are working through the backlog of issues older than that.

## Lifecycle Phases

### Unassigned

When an issue is first created, it may not be assigned to anyone and will not have a fix version. 

At this stage the issue has not been read by a staff committer.

### Waiting For Triage

Within a short period of time (usually a day or two), the issue is assigned to a specific committer and is also placed in the [Waiting for Triage](https://jira.springsource.org/issues/?jql=project%20%3D%20SPR%20AND%20fixVersion%20%3D%20%22Waiting%20for%20Triage%22) queue.

At this stage the issue has only been read superficially to the extent of ensuring it's not outright invalid, and recognizing whom it should be assigned to.

### Triaged

The assigned committer reviews the issue and either sets a fix version or resolves it with the appropriate resolution `Duplicate`, `Cannot Reproduce`, `Won't Fix`, `Invalid`, etc. Before doing so the committer may comment to ask for further information or request that [an issue project](https://github.com/SpringSource/spring-framework-issues#readme) be created to demonstrate the issue.

At this stage the issue has been looked at in sufficient detail and acknowledged as a valid request. The fix version indicates when it might be addressed.

The following describes the options for the assigned fix version:

* a specific version like `3.2 M2`, `3.2 RC1`, `3.2 RELEASE` -- provides a strong indication of when the issue may be resolved
* a version backlog like `3.2 Backlog` -- the issue is under consideration for the release
* the general backlog, `General Backlog` -- the issue is a valid request to consider for any release
* the contributors' queue, `Contributions Welcome` -- the issue is a valid request, and particularly well-suited to external contribution, i.e. is discrete and straightforward to implement. See the [Contributor Guidelines|https://github.com/SpringSource/spring-framework/blob/master/CONTRIBUTING.md] for more information.

If the issue is a bug, the fix version will likely be the next release. However, the next release may be a milestone and it may be a while before a final release is available. For such issues, the committer may create a sub-task of type "Backport" with the fix version set to an upcoming maintenance release like `3.1.2`. The backport task will track the resolution of the bug in the maintenance branch.

### In Progress

The committer begins working on an issue and either resolves it as `Complete` or marks it with the appropriate alternative resolution such as `Won't Fix`. This reflects the reality that although the issue may have had a fix version set for some time, by the time actual development begins, any number of events may have taken place (related code changes, new 3rd party libraries, new IETF or JSR specs, etc.), or the implementation may lead to a different decision than the one made at the time of triage.

### Resolved

At any time after an issue is resolved and before a final release becomes available, an issue may be re-opened.

### Closed

When a final (GA) release becomes available, all issues associated with the release, including milestones and release candidates, are closed and can no longer be re-opened.
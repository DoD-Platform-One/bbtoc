# Package Maintenance Tracks

## BBTOC Approval Process

A user must submit an issue to [the BBTOC](https://repo1.dso.mil/big-bang/product/bbtoc), show up to the meeting to present and request a decision on the issue, and upon being accepted work with the Big Bang team to get the work defined, scoped, and scheduled.

## Track Change Notification

Big Bang sending out a warning of the move of the package 90, 45, 30, 15, 7, 3, and 1 day before the move between tracks. This doesn't apply to new adoptions. Those notifications should be sent in:

- Big Bang Universe Slack [#announcements](https://bigbanguniver-ft39451.slack.com/archives/C050VKRU9HV) channel
- IL2 Platform One Mattermost Platform One Team [Value Stream - Big Bang](https://chat.il2.dso.mil/platform-one/channels/team---big-bang) channel
- IL4 Platform One Mattermost P1 Big Bang Team [Big Bang Release Engineering](https://chat.il4.dso.mil/p1-big-bang/channels/big-bang-release-engineering) channel
- IL4 Platform One Mattermost Platform One Team [All: Announcements](https://chat.il4.dso.mil/platform-one/channels/all-announcements) channel
- Included in the release notes of every release until the track change is complete
- Included in the Helm Upgrade Notes until the track change is complete

Example Track Change Notices:

```md
---
## ⚠️ ∭ -> 🧹 TRACK CHANGE NOTICE ∭ -> 🧹 ⚠️

MyApp

Jan 01, 0001

On Jan 01, 0001 MyApp will be transitioning from the Big Bang Integrated Track to the Big Bang Maintained Track. Please note that this means while the Big Bang team will still provide updates to this package and test it deployed in isolation (with wrapper in Big Bang Core), they will not: test it with the rest of Big Bang (including on demand and nightly k8s distribution specific tests), test it in production-like environments, or include it as a direct option in the Big Bang chart. This will also limit the support the Big Bang team will be able to provide for this package to its deployment in isolation.

---
```

```md
---
## ⚠️ 🧹 -> ֍ TRACK CHANGE NOTICE 🧹 -> ֍ ⚠️

MyApp

Jan 01, 0001

On Jan 01, 0001 MyApp will be transitioning from the Big Bang Maintained Track to the Community Maintained Track. Please note that this means this application will no longer get updates from the Big Bang Team. This will eliminate support the Big Bang team will be able to provide for this package. The new CODEOWNERS have been identified as @john.doe35 and @bob.smith12. If you would like to volunteer to be a CODEOWNER please reach out to the Big Bang team.

---
```

### Big Bang Integrated

This track includes packages that are owned and maintained by the Big Bang value stream, and are integrated to the Big Bang chart, i.e. all core and addon packages.

- **+ Big Bang Integrated**: To add new packages to this track a user must follow the [BBTOC Approval Process](#bbtoc-approval-process). After approval, the work will include, but isn't limited to: defining the upstream (if applicable), selecting a mission team to own the package, identifying security needs, and following the [Definition of Done Checklist](https://repo1.dso.mil/big-bang/team/team-charter/-/blob/main/docs/team_norms/new-gitLab-epic-checklist-template.md?ref_type=heads#definition-of-done-checklist).
- **-> Big Bang Maintained**: To move a package from BB Integrated to BB Maintained a user must follow the [BBTOC Approval Process](#bbtoc-approval-process). After approval, the [track change notifications](#track-change-notification) should begin as soon as possible. The work to move the package should not be released until the target date identified in the notification. That work will include, but is not limited to: updating the track badge, removing references in the Big Bang chart, updating the documentation to reflect its new deployment strategy (likely [wrapper](https://repo1.dso.mil/big-bang/product/packages/wrapper)).
- **-> Community Maintained**: This should be done by changing to Big Bang Maintained first. This is give customers that rely on the package longer to find alternatives. However, if it is known at the outset that a package will move all the way to Community Maintained that should be called out as an eventual goal in the track change notification.

### Big Bang Maintained

This track includes packages that are owned and updated by Big Bang, but will only be tested in isolation, e.g. package pipelines. The packages here will not be included in the Big Bang chart. The support that the community will receive will be limited to the package running in isolation, i.e. interactions with other package, networking issues, and emergent issues would not be supported.

- **-> Big Bang Integrated**: To move a package from BB Maintained to BB Integrated a user must follow the [BBTOC Approval Process](#bbtoc-approval-process). No notifications are required for this move. After approval, the work will include, but isn't limited to: updating the track badge, adding references in the Big Bang chart, updating the documentation to reflect its new deployment strategy (likely as a Big Bang Addon).
- **+ Big Bang Maintained**: To add new packages to this track a user must follow the [BBTOC Approval Process](#bbtoc-approval-process). After approval, the work will include, but isn't limited to: defining the upstream (if applicable), selecting a mission team to own the package, identifying security needs, and following the [Definition of Done Checklist](https://repo1.dso.mil/big-bang/team/team-charter/-/blob/main/docs/team_norms/new-gitLab-epic-checklist-template.md?ref_type=heads#definition-of-done-checklist).
- **-> Community Maintained**: To move a package from BB Maintained to Community Maintained a user must follow the [BBTOC Approval Process](#bbtoc-approval-process). After approval, the [track change notifications](#track-change-notification) should begin as soon as possible. Finding new CODEOWNERS is preferred, but not required. If they haven't been identified by the time the a notification is sent, it should request volunteers to become CODEOWNERS. The work to move the package should not be released until the target date identified in the notification. That work will include, but is not limited to: updating the track badge, removing references in the Big Bang chart, moving the repo to the third-party group, updating the documentation to reflect its new deployment strategy (likely [wrapper](https://repo1.dso.mil/big-bang/product/packages/wrapper)).

### Community Maintained

This track includes packages that are owned and updated by the community. The Big Bang team will not provide updates or support for these packages.

- **-> Big Bang Maintained**: To move a package from Community Maintained to BB Maintained a user must follow the [BBTOC Approval Process](#bbtoc-approval-process). No notifications are required for this move. After approval, the work will include, but is not limited to: updating the track badge, adding references in the Big Bang chart, moving the repo to the Big Bang Universe group, updating the documentation to reflect its new deployment strategy (likely as a Big Bang Addon).
- **-> Big Bang Integrated**: To move a package from Community Maintained to BB Integrated a user must follow the [BBTOC Approval Process](#bbtoc-approval-process). No notifications are required for this move. After approval, the work will include, but isn't limited to: updating the track badge, adding references in the Big Bang chart, moving the repo to the Big Bang Universe group, updating the documentation to reflect its new deployment strategy (likely as a Big Bang Addon).
- **+ Community Maintained**: To add new packages to this track a user must open an issue in the Big Bang repo and request the package be added to the Community Maintained track. The Big Bang team will create the repo and add a CODEOWNERS file with the user that requested the package as the CODEOWNER.

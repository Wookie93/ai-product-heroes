# Product Pain Points & Opportunities Analysis
*Summary of user problems, root causes, and FlowCraft alignment opportunities across major PM tools.*

---

## Table of Contents
1. [Asana](#asana)
2. [ClickUp](#clickup)
3. [Linear](#linear)
4. [Jira](#jira)
5. [Trello](#trello)
6. [Agile & General](#agile--general)

---

## Asana

### Global Dashboard & Reporting
**User Need:** User wants a global Asana dashboard showing on-time vs late, cycle times, throughput, and per-department/person productivity but is blocked by reporting, rules, and field limitations.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| No global cross-project dashboard showing on-time/late status, cycle time, and throughput. | Asana reporting is project-scoped and lacks workspace-level consolidated metrics. | Reporting / Visibility / Analytics |
| Hard to measure task cycle time and time-to-complete per person. | No built-in cycle/lead-time analytics or automatic timestamp capture for state changes. | Reporting / Visibility / Analytics |
| Rules and custom fields are insufficient to automate required tracking and metrics. | Automation capabilities are limited and inflexible for complex cross-project policies. | Integration / Automation |
| Difficulty breaking down metrics by department and individual across projects. | Fragmented project structures and limited cross-project filtering/grouping. | Reporting / Visibility / Analytics |
| Lack of clear tutorials or concrete guidance for building a master dashboard. | Sparse or confusing documentation and few ready-made templates for agency reporting. | Support / Documentation / Community |

**Alignment:** Matches FlowCraft's core need for lightweight, cross-project reporting, simple automations, and easy onboarding to help small teams gain workspace-level visibility.

**Opportunities:**
* Build a workspace-level dashboard aggregating on-time, late, cycle time, and throughput.
* Provide cross-project filters by team, department, and individual.
* Auto-capture cycle-time via state-change timestamps and lightweight automations.
* Ship prebuilt dashboard templates and step-by-step onboarding for agencies.
* Offer Asana import/mapping to preserve fields, comments, and timestamps.

### Automation Failures & Data Integrity
**User Need:** Asana admin outlines 12–16 failure classes and concise checks to stop duplicate writes, rule loops, schema drift, webhook replays, and inconsistent rollups in rule-driven Asana setups.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Duplicate tasks and comment storms after webhook retries or worker restarts. | No idempotency or dedupe_key; multiple writers reapply same mutation. | Integration / Automation |
| Rules create loops across multi-home projects, flipping task state repeatedly. | Multiple autonomous agents mutate tasks without a single-writer or revision checks. | Workflow / Process |
| Custom field renames or enum changes break downstream scripts and syncs. | Consumers rely on display names rather than stable field GIDs. | Integration / Automation |
| Portfolio and project rollups disagree, producing inconsistent status reports. | No single source-of-truth snapshot; rollups computed from different times/sources. | Reporting / Visibility / Analytics |
| Webhook sync tokens invalidate causing missed updates, floods, and replayed writes. | Lack of token recovery strategy and replay suppression during backfill. | Reliability / Bugs / Stability |

**Alignment:** These automation, integration, and reporting failure modes directly threaten adoption of collaboration, sprints, and reporting—core areas FlowCraft must stabilize for teams scaling past 15–30 people.

**Opportunities:**
* Provide built-in idempotency keys and dedupe analytics for integrations.
* Offer a single-writer mutation queue to serialize rule and automation writes.
* Add automated schema probes and field-GID contracts with daily validation alerts.
* Implement snapshot-based rollups with explicit snapshot ids and authoritative source selection.
* Offer webhook sync recovery with time-window backfill and replay suppression flags.

### Agency Budgeting & Time Tracking
**User Need:** Agency with ~10 staff seeks project and staff time-budgeting and per-person estimated-vs-actual reporting; current tools (Asana/Harvest) don’t provide needed visibility across differing team workflows.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| No project-level time budgets to track retainers monthly against actual hours. | Tool lacks native project budget/actual time linkage and alerts. | Reporting / Visibility / Analytics |
| No staff-level budgeting or weekly contracted-hours visibility per employee. | Time entries aren’t surfaced as per-user capacity dashboards. | Reporting / Visibility / Analytics |
| Unable to produce graphs comparing estimated time versus actual time at staff-by-staff level. | Reporting filters and data model don’t join estimates, time entries, and user attribution. | Reporting / Visibility / Analytics |
| Divergent team workflows (SEO uses due-dates/calendar; dev uses sprint sections) hinder consolidated reporting. | Inconsistent metadata (due dates vs sections) prevents unified aggregation across teams. | Workflow / Process |
| Reluctance to fully replace Harvest because it provides superior time-tracking visibility. | Feature gap between current PM tool’s time tracking and dedicated time-tracking product. | Integration / Automation |

**Alignment:** Directly matches FlowCraft’s need to improve reporting, staff/project budgeting, and cross-workflow visibility for 5–50 person teams.

**Opportunities:**
* Add project retainer budgets with real-time actual-vs-budget tracking and monthly alerts.
* Provide per-staff weekly contracted-hours dashboards and overage warnings.
* Build per-user estimated vs actual graphs and exportable reports.
* Normalize task metadata to support both calendar due-dates and sprint-section workflows.
* Offer Harvest import/mapping and a native lightweight time-tracking integration.

### Migration & API Issues (Tag Colors)
**User Need:** Team migrating Asana-to-Asana encountered breaking tag APIs: Asana renamed tag color names, GET returns old names, create endpoint makes colorless tags and returns mismatched colors.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Asana renamed tag color names; GET endpoint still returns old names. | API contract change without backward-compatible mapping or versioning. | Migration / Adoption / Onboarding |
| Tag creation API accepts color but creates colorless tags and returns incorrect colors. | Backend regression or incorrect color handling in the create-tag endpoint. | Reliability / Bugs / Stability |
| API responses and documentation are inconsistent. | Documentation lag and inconsistent API rollout/versioning. | Support / Documentation / Community |
| Migrations risk losing metadata (colors) and require manual validation. | Lack of validation, dry-run checks, and robust import semantics in migration tooling. | Migration / Adoption / Onboarding |

**Alignment:** Integration and migration failures that directly impede FlowCraft’s import/migration experience.

**Opportunities:**
* Provide import tool with automatic tag-color mapping and editable mappings.
* Add dry-run validations to detect API-contract mismatches before writes.
* Ship adapters that translate Asana API versions and legacy names.
* Expose detailed import logs and rollback for metadata fidelity.
* Monitor third-party API changes and alert admins to breaking changes.

### Downgrade Experience & Paywalls
**User Need:** User locked out of an Asana project after downgrading a free trial; premium custom fields/timeline block access, CSV export loses attachments and subtasks, and upgrade/seat UX is confusing.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Project becomes inaccessible after downgrading; paywall requires minimum two seats. | Premium feature gating that enforces minimum-seat billing and blocks visibility on downgrade. | Pricing / Licensing / Value |
| Cannot remove custom fields without upgrading, preventing project edits. | Premium feature artifacts persist and require paid plan to modify or remove. | Migration / Adoption / Onboarding |
| CSV export loses attachments, links, and breaks subtask-parent relationships. | Export format lacks relational fidelity and does not include media or hierarchical context. | Migration / Adoption / Onboarding |
| Inconsistent upgrade prompts and unclear collaborator vs user semantics. | Ambiguous role definitions and inconsistent UI messaging across workspace users. | Usability / UX / UI |

**Alignment:** Project-locking paywalls and poor export fidelity threaten smooth migration and retention.

**Opportunities:**
* Allow downgrades without locking projects; enable removal of premium fields without payment.
* Provide high-fidelity export/import preserving attachments, links, and task hierarchy.
* Offer single-seat or prorated upgrades for solo/small users.
* Clarify collaborator vs user roles and make upgrade prompts consistent.
* Add pre-downgrade checklist or reminders to remove premium features.

### Security (MCP Bug & Trust)
**User Need:** User cites Asana MCP bug exposing other orgs' data for 34 days and asks if it reduces trust and what safeguards prevent AI agents from corrupting projects/data.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| AI/agent access could expose other organizations' data. | Broad MCP permissions and insufficient isolation between organization contexts. | Security / Privacy / Compliance |
| Long incident window and high remediation cost reduce confidence. | Slow detection, response, and inadequate monitoring of agent-facing services. | Security / Privacy / Compliance |
| Fear that AI agents could perform destructive actions on projects/data. | Lack of bounded automation, approval gates, and safe-mode for automated actions. | Integration / Automation |
| Teams may delay or avoid adopting MCP/AI integrations. | Loss of trust due to security incidents and unclear safety guarantees. | Migration / Adoption / Onboarding |
| Insufficient visibility and audit trails for agent actions. | Limited logging, traceability, and tooling for inspecting automated changes. | Reporting / Visibility / Analytics |

**Alignment:** Security, permissions, and trustworthy automation directly impact startups' willingness to adopt advanced collaboration features.

**Opportunities:**
* Implement least-privilege, org-scoped agent permissions and default-deny policies.
* Provide time-bound, revocable roles for contractors and agents.
* Ship immutable, searchable audit logs for all agent actions.
* Require approval gates and sandboxed simulation for destructive agent operations.
* Publish security posture: pen-tests, incident timelines, and certifications.

---

## ClickUp

### Lists & Project Management Limitations
**User Need:** User says ClickUp Lists lack project-level status, filterable start/end dates, list custom fields, and list-specific views, making project management unmanageable for a medium-sized business.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Lists have no true status field; 'Color' is confusing and cannot be filtered. | Lists were implemented without first-class status metadata or list-level filtering. | Workflow / Process |
| Start and end dates on Lists aren’t filterable or exportable via API. | Date fields exist superficially but lack query/export capabilities for reporting. | Reporting / Visibility / Analytics |
| Lists cannot have custom fields. | List-level metadata was excluded from the custom-field model reserved for tasks. | Customization / Flexibility |
| Overview and Portfolio widgets lack filtering and grouping. | Aggregate widgets don’t support granular list-level filters or group-by controls. | Reporting / Visibility / Analytics |
| Lists are unmanageable at medium scale, blocking portfolio views. | Tool treats projects as lightweight containers without project-scale features. | Scalability / Performance |

**Alignment:** Addresses FlowCraft’s core need: first-class project entities and filtered portfolio views to retain growing (30–50+) teams.

**Opportunities:**
* Make projects first-class entities with renameable, filterable status fields.
* Add filterable start/end date fields and expose them via API for BI exports.
* Enable list-level custom fields and project templates for teams/products.
* Provide list-specific filtered/grouped views and portfolio dashboards.
* Offer migration tools/mappers for Trello/Notion/ClickUp lists to project entities.

### Sprint Snapshots & Git Integration
**User Need:** Scrum Master cannot preserve an immutable snapshot of sprint delivery in ClickUp; moving or duplicating carry-over tasks breaks sprint history or Git links.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| No immutable end-of-sprint snapshot preserving each task's status. | ClickUp removes tasks from a sprint when moved, with no read-only archive of sprint state. | Reporting / Visibility / Analytics |
| Carried-over tasks lose original custom IDs or require duplication, breaking Git. | Task duplication or reassignment severs the external-ID-to-Git linkage. | Integration / Automation |
| Using one task in multiple lists causes later edits to change prior sprint records. | Single-entity-in-multiple-sprints shares live state rather than creating per-sprint copies/snapshots. | Workflow / Process |
| No lightweight sprint-closing workflow that preserves historical context. | Lack of a built-in sprint closure/archive feature tailored to Scrum reporting needs. | Migration / Adoption / Onboarding |

**Alignment:** Directly relates to sprint reporting, task lifecycle, and Git integrations—core barriers for engineering teams.

**Opportunities:**
* Provide read-only sprint snapshots that record task statuses and metadata at sprint close.
* Support persistent external IDs and preserve Git links when moving or cloning tasks.
* Offer 'carry-over' flow that links next-sprint work while preserving prior-sprint history.
* Enable exportable per-sprint reports (CSV/JSON) with task state and ID mapping.
* Add a lightweight sprint-close archive action that timestamps and freezes sprint data.

### Reliability, Bugs & Support
**User Need:** A 17-seat team reports multiple ClickUp bugs (scheduling, notifications, calendar, docs) causing rescheduling, missed updates, extra work, and potential migration consideration.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Unpredictable scheduling and dependency bugs (tasks moved to weekends). | Faulty scheduling/dependency engine or state-sync causing server-side overrides. | Reliability / Bugs / Stability |
| Delayed inbox notifications leading to missed updates. | Notification delivery latency or queueing and integration delays. | Collaboration / Communication |
| Broken calendar and content rendering. | UI/rendering bugs and regressions affecting calendar and document views. | Reporting / Visibility / Analytics |
| Slow, opaque support responses. | Insufficient incident communication and prioritization from vendor support. | Support / Documentation / Community |
| Operational overhead: team built manual protocols to compensate for instability. | Core feature instability forcing duplicative manual workflows and tracking. | Migration / Adoption / Onboarding |

**Alignment:** Explicit reliability and support failures map directly to FlowCraft’s need to prevent churn and enable scalable PM.

**Opportunities:**
* Ship a deterministic scheduling/dependency engine with audit trail and reversible changes.
* Provide real-time inbox, low-latency notifications, and actionable Slack integration.
* Offer a public incident dashboard with bug statuses, timelines, and ETAs.
* Build accurate ClickUp import preserving dates, comments, dependencies, and history.
* Include templates and rule-based automations preventing unintended rescheduling.

### Gantt & Scheduling Bugs (Year 2081)
**User Need:** ClickUp's Gantt view bug auto-sets moved tasks' due dates to year 2081, disrupts teams relying on dependencies and frequent Gantt rescheduling.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Gantt moves assign incorrect extreme dates (year 2081). | Regression in Gantt date-handling logic causing incorrect date assignments during drag/move. | Reliability / Bugs / Stability |
| Dependency-based scheduling breaks; moving tasks triggers cascading wrong dates. | Automatic dependency recalculation applies faulty date offsets without validation. | Workflow / Process |
| Operational overhead: teams must manually fix dates dozens of times daily. | No safe-undo or bulk correction tools to revert erroneous date changes. | Productivity / Focus |

**Alignment:** Reliability and dependency-scheduling failures.

**Opportunities:**
* Implement guarded Gantt moves with date-validation and confirm-before-apply.
* Provide dependency-aware move previews and one-click rollback for moved tasks.
* Offer bulk-date correction and revert tooling for affected tasks.
* Add sane default date ranges and anomaly alerts.

### AI Agents & Hierarchy
**User Need:** ClickUp AI agents ignore manual task sort and hierarchy, causing incorrect 'Next Action' promotions within GTD-style projects.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Agents can’t read manual/custom sort order. | API/agent does not expose or honor UI-specific ordering. | Integration / Automation |
| Agents don’t reliably follow parent→child hierarchy and promote across projects. | Automation logic flattens or misinterprets hierarchical relationships. | Workflow / Process |
| No easy way to limit active 'Next Actions' per project. | Lack of configurable, scoped promotion rules per project. | Customization / Flexibility |

**Alignment:** Need for simple, hierarchy-aware automations and integrations that preserve user ordering.

**Opportunities:**
* Expose UI/manual ordering via API for automations to consume.
* Add hierarchy-aware automation that scopes promotions to parent projects.
* Provide per-project concurrency settings for active 'Next Actions'.
* Offer non-date prioritization controls (priority lanes, quick-reorder badges).

---

## Linear

### Scaling, Recurring Tasks & Mobile
**User Need:** Seeker wants a fast, polished PM tool with true recurring tasks, powerful automations, and a native iOS app; currently personal use but needs scalability for freelancers.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Lack of true recurring tasks (scheduled and 'on completion'). | Many PM tools provide simple repeating reminders rather than workflow-triggered recurring items. | Workflow / Process |
| Insufficient automation for task management (e.g., move/archive). | Limited or rigid automation engines that don't support conditional or rule-based actions. | Integration / Automation |
| Poor native mobile experience—iOS apps that are laggy web wrappers. | Products prioritizing web parity over native performance. | Usability / UX / UI |
| Tools skewed toward developer workflows rather than general-purpose PM. | Design and feature prioritization favor engineering use-cases. | Customization / Flexibility |
| Need for scalability to manage freelancers without complex setup. | Lack of lightweight roles, temporary access, and simple contractor workflows. | Permissions / Security |

**Alignment:** Maps to FlowCraft’s mission: fast, simple PM with automations, native mobile performance, and scalable contractor workflows.

**Opportunities:**
* Implement true recurring tasks: scheduled and on-completion variants.
* Provide rule-based automations to move/archive tasks without due dates.
* Ship a fast native iOS app (not a web wrapper) with offline responsiveness.
* Add simple, time-bound contractor roles and lightweight scalability features.

### View Portability & Scoping
**User Need:** User is unsure where to store project views (team Views vs Projects tab vs workspace), forced to duplicate views in multiple places and cannot move views between scopes.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Cannot move or transfer a view between team and workspace sections. | UI restricts view ownership to a single scope with no portability feature. | Customization / Flexibility |
| Duplicate copies of the same project view across locations cause maintenance overhead. | No canonical/shared view model or single source of truth for views. | Workflow / Process |
| Unclear visibility and scope semantics between workspace and team views. | Insufficient UI affordances explaining scope and access implications. | Reporting / Visibility / Analytics |

**Alignment:** Relates to cross-team/portfolio visibility, consolidation, and UX.

**Opportunities:**
* Allow moving/porting views between team and workspace scopes while preserving filters.
* Introduce canonical/shared views with scope overrides to avoid duplication.
* Provide a workspace-level portfolio view aggregating team projects.
* Add pin/subscribe or link-to-view features to surface views without copying them.

### Migration from GitHub/Context
**User Need:** User spends 15–20 minutes gathering multi-repo code context before using an AI assistant from a Linear issue.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Manual, time-consuming context gathering per multi-repo issue. | Issue tracker lacks automated cross-repo context capture and code search integration. | Workflow / Process |
| No integrated cross-repo search or auto-linking to surface relevant files. | Code and history live separately from the issue tracker; connectors are missing. | Integration / Automation |
| AI assistant effectiveness depends on fully enriched prompts. | AI tools don’t automatically assemble repository context for a given issue. | Collaboration / Communication |

**Alignment:** Missing integrations, cross-repo visibility, and productivity gaps.

**Opportunities:**
* Auto-attach cross-repo context (relevant files, snippets, and PRs) when creating issues.
* Deep GitHub integration: code search, pattern matching, and PR linking from tasks.
* AI-assisted issue composer that gathers repository context automatically.
* Multi-repo task templates/checklists with DoR items and example references.

### Customer Feedback & Triage
**User Need:** User struggles to integrate customer feedback in Linear; converting feedback into projects loses context, and they need a triage workflow.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Converting feedback into projects removes or hides original context. | Tool doesn't propagate or preserve feedback references/metadata when creating projects. | Workflow / Process |
| No standardized triage/holding area for varied-sized requests. | Lack of built-in request staging patterns, templates, or team-level holding workflows. | Workflow / Process |
| Hard to maintain a visible link between customer input and delivery status. | Missing parent-child linking or automatic metadata propagation across issue→project promotion. | Reporting / Visibility / Analytics |

**Alignment:** FlowCraft’s need for unified backlog-to-project workflows and feedback traceability.

**Opportunities:**
* Preserve and surface original feedback links when converting items into projects.
* Offer a built-in 'Requests' holding board/team with triage states and templates.
* Add parent-child linking and automatic metadata propagation from feedback to projects.
* Expose reporting that traces feedback-to-delivery status.

### GitHub Automation Triggers
**User Need:** Broad GitHub automation triggers in Linear cause merged/approved issues to revert to Code Review (e.g., branch deletion counts as activity).

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Broad triggers move merged issues back to Code Review after branch-delete activity. | Rule uses a generic 'or activity' clause; branch deletion counts as activity. | Integration / Automation |
| Commits made after approval revert issues back into Code Review. | Automations don't distinguish post-approval commits from relevant review events. | Workflow / Process |
| Cannot create individual, customizable rules. | Limited rule granularity and lack of trigger filters. | Customization / Flexibility |

**Alignment:** Need for reliable integrations and lightweight workflow automations.

**Opportunities:**
* Expose per-event trigger granularity (separate PR-review, PR-activity, merge events).
* Allow filters to ignore branch-deletion or post-merge activity.
* Support rule scoping by repo, branch, actor, or event type.
* Add terminal-state protections to prevent post-merge status regressions.

---

## Jira

### Scheduling & Resource Limits
**User Need:** Production lead blocked by single-assignee model, basic licences, no marketplace add-ons, and political resistance to change (Excel reliance).

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Single-assignee model prevents accurate dynamic two-person assignments. | Platform limitation combined with license constraints forces text fields/duplicates. | Workflow / Process |
| No unified long-term calendar or capacity view. | Basic licences and siloed projects block cross-project timeline and reporting. | Reporting / Visibility / Analytics |
| Excel remains the canonical schedule. | Pre-production ownership, management scepticism, and voluntary adoption politics. | Migration / Adoption / Onboarding |
| Company policy forbids marketplace add-ons. | Budget/policy restrictions limit available features. | Pricing / Licensing / Value |

**Alignment:** FlowCraft’s ICP are 5–50 person teams that need lightweight scheduling and multi-assignee workflows.

**Opportunities:**
* Support multi-assignee/role-per-issue with lightweight role semantics.
* Built-in resource calendar with capacity planning and overlayed constraints.
* Cross-project, shareable constraint view without premium features.
* One-click Excel import/export to ease migration.

### Board & Release Management
**User Need:** Jira boards refuse to persist status column order. Release management feels clunky with poor visibility and manual steps.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Cannot reorder status columns; statuses always land at the end. | Backend order-persistence bug or corrupted per-board configuration. | Reliability / Bugs / Stability |
| Generic, non-actionable error message. | Poor error handling and lack of diagnostic feedback. | Support / Documentation |
| Poor visibility into what is included in a release. | Release metadata scattered across views; not surfaced in a release-centric view. | Reporting / Visibility / Analytics |
| Release process disconnected from deployment pipelines. | Lack of reliable integrations surfacing build/deploy statuses within release workflows. | Integration / Automation |

**Alignment:** Board reliability and release visibility impact retention.

**Opportunities:**
* Provide persistent, explicit column ordering controls with save/versioning.
* Show actionable error messages with remediation steps.
* Release-centric timeline showing included issues, statuses, and deployment targets.
* Bi-directional CI/CD integration surfacing build/deploy status.

### Hierarchy & Configuration Governance
**User Need:** Hierarchy misconfiguration (Story = Epic level) broke parent-child links. Centralized config control causes 1-2 week delays for PMs.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Story set to same level as Feature/Epic, breaking relationships. | Work type levels misconfigured in settings. | Workflow / Process |
| Any configuration change requires central admin approval (delays). | Governance model funnels all changes through central admin team. | Workflow / Process |
| Teams lack self-service ability to create projects/fields. | Restricted permissions and absence of delegated configuration roles. | Migration / Adoption / Onboarding |

**Alignment:** Onboarding friction and hierarchy/permission rigidity.

**Opportunities:**
* Add a hierarchy-change preview simulator showing affected issues.
* Offer scoped self-service project and field configuration with audit trails.
* Provide time-bound, least-privilege roles for teams.
* Build a bulk remapping wizard to re-parent child links safely.

### Migration & UI Redesign
**User Need:** User upset about Jira's major UI redesign (navigation swapped, denser layout) requiring re-learning.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Navigation elements rearranged, breaking muscle memory. | Large, non-optional redesign changed established info architecture. | Usability / UX / UI |
| Denser, closer-together layout feels messy. | UI density choices reduced visual clarity. | Productivity / Focus |
| Users must consult external tutorials to relearn workflows. | Insufficient in-app onboarding/tours for major changes. | Migration / Adoption / Onboarding |

**Alignment:** Disruptive redesigns harm usability and retention.

**Opportunities:**
* Provide a stable, minimal-change UI promise and clear versioning.
* Offer in-app guided tours for any UI changes.
* Include an opt-in 'classic view' toggle during major redesigns.

---

## Trello

### Search & Discoverability
**User Need:** User reports Trello's search fails to find existing cards, causing fear of lost items.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Search returns no results for existing cards. | Search indexing or workspace-scoping bug. | Reliability / Bugs / Stability |
| Unreliable search undermines confidence. | Inconsistent discoverability creates distrust. | Reporting / Visibility / Analytics |
| Perceived product priorities favor new features over core stability. | Roadmap deprioritizes essential stability/search improvements. | Usability / UX / UI |

**Alignment:** Reliable search is critical for retention.

**Opportunities:**
* Fix search indexing to guarantee discoverability.
* Add search QA, monitoring, and alerting.
* Expose clear scope/filters and show matching board/card previews.

### Deprecation of API Tokens
**User Need:** Atlassian plans to deprecate Trello API tokens for OAuth2, breaking automations and integrations for small businesses.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Mass breakage of automations/integrations built on tokens. | Deprecation of API tokens without backward compatibility. | Integration / Automation |
| High migration cost and disruption. | Forced migration with no transition path. | Migration / Adoption / Onboarding |
| Erosion of trust and existential business risk. | Unilateral product change and vendor silence. | Emotional / Motivational |

**Alignment:** Integration breakage drives migration demand.

**Opportunities:**
* Offer a Trello-compatibility layer that accepts legacy API tokens.
* Build migration/import tools to port Trello automations into FlowCraft.
* Position FlowCraft as stable and developer-friendly.

### Automation Limitations (Butler)
**User Need:** User cannot automate moving checklist items *within* a card, or target the *top* of a list when a limit is reached.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Butler lacks action to move checklist items between checklists on same card. | No intra-card checklist-move action. | Integration / Automation |
| Automation cannot target the top card (only bottom-of-list). | Feature set limits positional targets. | Integration / Automation |
| No documented workaround. | Limitations of Butler's cross-card copy patterns. | Workflow / Process |

**Alignment:** Need for expressive, rule-based automations.

**Opportunities:**
* Add intra-card 'move checklist items' automation action.
* Support position-aware automation: top/bottom/index selectors.
* Provide built-in 'overflow' templates (when list > N, move oldest).

### Visual & UI Changes
**User Need:** Removal of list/column background colors broke visual organization. New Gantt/Planner features disrupt Kanban workflows.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Removal of background colors eliminated key visual cues. | Design change removed legacy customization feature. | Usability / UX / UI |
| New planner/Gantt and checkmarks disrupt simple Kanban. | Default-on feature additions prioritize new views over core Kanban. | Usability / UX / UI |
| No opt-out for unwanted features. | Lack of granular feature toggles. | Customization / Flexibility |

**Alignment:** FlowCraft can offer stable, customizable Kanban.

**Opportunities:**
* Provide granular list/column color customization.
* Add per-user/per-board feature toggles (Kanban-first mode).
* Offer legacy mode or opt-out for major UI changes.

---

## Agile & General

### AI in Agile
**User Need:** Poster requests ideas for AI-enabled Agile to integrate with status updates, ceremonies, and sprint data to reduce overhead.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Lack of actionable insights from sprint data. | Fragmented data; no automated synthesis. | Reporting / Visibility / Analytics |
| Ceremony overhead and meeting fatigue. | Synchronous, manual ceremonies without async alternatives. | Productivity / Focus |
| Agile metrics are noisy or manual. | Metrics require manual aggregation. | Reporting / Visibility / Analytics |
| Poor cross-team coordination. | Lack of automated dependency detection. | Scalability / Performance |

**Alignment:** FlowCraft seeks to increase adoption of collaboration/sprints while reducing overhead.

**Opportunities:**
* AI-generated executive summaries and sprint health dashboards.
* Asynchronous AI standup summarization.
* Automated risk predictions and dependency detection.

### Roles & Process Confusion
**User Need:** Confusion about Project Manager vs Product Owner vs Scrum Master roles; new Scrum Masters overwhelmed by coordination.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Unclear role boundaries cause confusion. | Startups lack documented RACI or role charters. | Collaboration / Communication |
| Overwhelmed coordinating multiple teams. | Single coach assigned too many teams without tooling support. | Scalability / Performance |
| Lack of onboarding for roles. | Teams compress roles or lack training. | Migration / Adoption / Onboarding |

**Alignment:** Clarifying roles and providing templates aids scaling.

**Opportunities:**
* Ship opinionated role templates (PM/PO/SM) with responsibilities.
* Provide cross-team dashboards surfacing team health.
* Offer async status capture to reduce meeting volume.

### Acceptance Criteria & Estimation
**User Need:** Team lacks written acceptance criteria (AC) before sizing; estimates treated as fixed commitments by management.

**Problems & Root Causes:**
| Problem | Root Cause | Category |
| :--- | :--- | :--- |
| Missing AC causes estimation variability. | No agreed Definition of Ready (DoR). | Workflow / Process |
| Estimates treated as promises/commitments. | Management lacks agile literacy; demands fixed numbers. | Workflow / Process |
| Epics pre-estimated at high level. | Process requires pre-existing estimates for approval. | Reporting / Visibility |

**Alignment:** Gaps in reporting and forecasting for small teams.

**Opportunities:**
* Visualize estimation ranges/confidence.
* Provide Sprint Goal templates and DoR/DoD policy checks.
* Manager-facing guides on estimation uncertainty vs predictability.

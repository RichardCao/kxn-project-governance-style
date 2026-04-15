# Evidence Matrix

## 1. `#40` Issue And Doc Synchronization

- Issue claim:
  - issue-driven work needs a path back into canonical docs
  - the sync must be incremental and timestamp-aware
- Commits:
  - `72f3c38`
  - `40df28b`
  - `e0f1d74`
- Anchors:
  - `.codex/state/issue-doc-sync/state.json`
  - `docs/general/feishu-product-design.md`
  - `docs/general/install-deploy-design.md`
  - `docs/general/relay-protocol-spec.md`
  - `docs/general/user-guide.md`
- Style inference:
  - docs are treated as a governance surface
  - process memory is externalized into tracked state instead of left implicit

## 2. `#70` Workspace-First Thread Ownership

- Issue claim:
  - thread handling should be pulled back under workspace-first semantics
- Commits:
  - `a92932b`
  - `95094d5`
  - `1f14e72`
  - `ac04cde`
  - `be94efa`
- Anchors:
  - `internal/core/orchestrator/service_routing.go`
  - `internal/core/orchestrator/service_surface.go`
  - `internal/core/orchestrator/service_thread_global.go`
  - `internal/adapter/feishu/projector.go`
  - `internal/core/orchestrator/service_test.go`
  - `docs/general/remote-surface-state-machine.md`
- Style inference:
  - source-of-truth semantics outrank shortcut convenience
  - staged delivery is followed by semantic corrections and presentation cleanup

## 3. `#140` Detection-Driven Onboarding

- Issue claim:
  - setup should be driven by detected capability and current decision state, not by legacy wizard completion ticks
- Commits:
  - `bb478a8`
  - `17839e1`
  - `1be12fa`
  - `77c4342`
  - `7a60a56`
- Anchors:
  - `docs/draft/web-onboarding-admin-user-mock.html`
  - `web/src/routes/SetupRoute.tsx`
  - `web/src/routes/SetupRoute.test.tsx`
  - `web/src/routes/setup/SetupStepContent.tsx`
  - `web/src/routes/setup/helpers.ts`
  - `internal/app/daemon/admin.go`
- Style inference:
  - product language and information architecture are governed as primary work
  - mocks, implementation, tests, and routing cleanup form one execution chain

## 4. `#160` UI Boundary Refactor

- Issue claim:
  - the orchestrator should stop directly owning surface-specific DTO and view assembly details
- Commits:
  - `ffd0fed`
  - `cb0a543`
  - `2d2eec8`
  - `b602a63`
  - `b7b7f52`
  - `14d6d16`
- Anchors:
  - `internal/core/control/feishu_ui_boundary.go`
  - `internal/core/orchestrator/service_feishu_ui_context.go`
  - `internal/core/orchestrator/service_feishu_ui_controller.go`
  - `internal/adapter/feishu/projector_selection_view.go`
  - `internal/adapter/feishu/projector_command_view.go`
  - `internal/core/control/feishu_ui_intent_test.go`
  - `internal/adapter/feishu/projector_test.go`
  - `docs/general/feishu-card-ui-state-machine.md`
- Style inference:
  - maintainability is promoted into a planned phase
  - ownership cleanup is part of delivery, not postponed indefinitely

## 5. `#180` Token Usage Shared Substrate

- Issue claim:
  - thread-level and turn-level usage views should share one stable data substrate
- Commits:
  - `aa15701`
  - `8ab5ab2`
- Anchors:
  - `internal/core/agentproto/token_usage.go`
  - `internal/adapter/codex/translator_token_usage.go`
  - `internal/core/orchestrator/service_token_usage.go`
  - `internal/adapter/feishu/projector.go`
  - `internal/core/orchestrator/service_test.go`
  - `internal/adapter/feishu/projector_snapshot_final_test.go`
  - `docs/general/relay-protocol-spec.md`
- Style inference:
  - build the shared model first
  - then expose it through the visible surface

## 6. `#200` Request-User-Input Effect Alignment

- Issue claim:
  - semantic parity is insufficient if the user interaction model still feels wrong
- Commits:
  - `d679866`
  - `4653682`
  - `9a353bc`
  - `a8aa33c`
  - `1b31463`
- Anchors:
  - `internal/core/orchestrator/service_request.go`
  - `internal/core/orchestrator/service_helpers_request.go`
  - `internal/core/state/types.go`
  - `internal/adapter/feishu/projector_request.go`
  - `internal/core/orchestrator/service_local_request_test.go`
  - `internal/adapter/feishu/projector_test.go`
  - `docs/general/feishu-card-ui-state-machine.md`
  - `docs/general/remote-surface-state-machine.md`
- Style inference:
  - deliver in stages, then refine until the interaction model matches intent
  - docs and tests move with each behavior shift

## 7. `#220` Unified Preview Fallback

- Issue claim:
  - fallback file preview should be a bounded, reusable, product-grade path
- Commits:
  - `c5373f3`
  - `ce374ee`
  - `e36000c`
  - `d83e9f8`
  - `d475a29`
  - `685b109`
- Anchors:
  - `internal/adapter/feishu/web_preview_registry.go`
  - `internal/adapter/feishu/web_preview_render.go`
  - `internal/adapter/feishu/web_preview_cleanup.go`
  - `internal/app/daemon/web_preview.go`
  - `internal/adapter/feishu/markdown_preview_concurrency_test.go`
  - `internal/adapter/feishu/web_preview_render_test.go`
  - `internal/app/daemon/app_preview_lock_test.go`
- Style inference:
  - fallback and recovery semantics are promoted into the mainline
  - concurrency and lifecycle risks are addressed immediately after first delivery

## 8. `#227` Final Reply Markdown Link Stabilization

- Issue claim:
  - keep the V2 path and fix root cause instead of escaping via rollback
- Commits:
  - `c64dc9d`
  - `525b037`
  - `a765534`
- Anchors:
  - `internal/adapter/feishu/final_card_markdown.go`
  - `internal/adapter/feishu/projector_final_markdown_links_test.go`
  - `docs/general/feishu-product-design.md`
  - `docs/implemented/feishu-md-preview-design.md`
  - `.codex/skills/issue-workflow-guardrail/SKILL.md`
- Style inference:
  - diagnose compatibility problems inside the intended architecture
  - feed the lesson back into guardrails, docs, and tests

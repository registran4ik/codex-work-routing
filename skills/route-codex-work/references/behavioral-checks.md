# Behavioral validation

Use these cases to review an installed profile or instruction change. Substitute real paths and tests from the repository. Do not run live writes to test the router. Expected decisions below are examples for a self-review; an independent evaluator should receive the request and raw artifacts without the intended answer.

| Request / condition | Appropriate routing decision |
|---|---|
| Correct one label in an established page | L0, exact fragment and preview; no archive or architecture audit |
| Adjust a component's keyboard behavior | L1, component and accessibility check; no unrelated backend reading |
| Change one permission condition | L3 even for one line; allow/deny cases and consumer boundary |
| Fix a spelling error in an auth page | L0 if authentication behavior is untouched; filename alone does not raise risk |
| Add a field across form and API | L2; follow existing validation/storage contract and boundary test |
| Change a payment callback | L3, replay/idempotency/failure cases; no actual charge implied |
| Rename a generated output | Identify generator and consumers; do not hand-edit a large generated tree |
| Replace a shared storage abstraction | L3/L4 by impact; callers, compatibility, staged validation/recovery |
| A test fails because a fixture lacks a dependency | Classify fixture/setup failure; do not blame product/model or rerun blindly |
| External publish times out after submission | Outcome UNKNOWN; readback before retry, no new writer |
| Task is urgent but independent work cannot be separated | Choose sufficient reasoning; urgency is not automatic orchestration |
| Three independent parts share one database migration | The migration remains one writer and a sequential dependency |
| Model selection was sent to an active task | Requested/pending, not observed until relevant runtime evidence |
| The account meter falls by a few percentage points | No task/model price attribution; disclose concurrent/unobserved work |
| Quota resets while the user has paused product work | Keep that pause until its authorized resumption condition is met |
| A later direct exception conflicts with a general stop policy | Preserve the scoped exception with its source; do not broaden it |
| Required command cannot be found | UNKNOWN; do not invent a runner or claim a passing test |
| A shorter instruction file passes a syntax validator | Structural success only; replay real routes before claiming usefulness |

Acceptance record: request, selected level and reason, first files, required conditional reference, actual/available check, model/effort rationale, known gap, and authority boundary. Validate at least ten real repository cases for a map-building task. Preserve failing cases and report whether the review was manual, executable, or independent; none of those is a product smoke by itself.

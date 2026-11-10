# keymanager: known issues (baseline debt)

Baseline `crewline testcase --scope all` @ 772f1659 (2026-11-10): 0 blocking, 0 warnings, 0 info. No validator debt recorded.

## KI-KEYMANAGER-001: no coverage matrix (Inferred)
`api-test/src/main/resources/coverage/` does not exist. The coverage matrix is the single source of truth for test cases
in this test stack, so bootstrap it with `CoverageCli init --module-root api-test --module-code KEYMANAGER` as a separate task.

# Coding-standards proposal: keymanager (DRAFT)

No checker was found, so `crewline coding-standards` only blocks debug leftovers in this repository (STD-004). It does not check style.
Crewline does not invent a standard; these are the usual checkers for what this repository contains. The module owner decides.

| Stack | Usual checker | Command for `crewline run` |
|---|---|---|
| Maven / Java | Spotless (`spotless-maven-plugin`) or Checkstyle (`maven-checkstyle-plugin`) | `mvn -B spotless:check` |

If the owner agrees:
1. Add the checker in its own small PR (a `documentation` or `refactor` task), with no mass reformat.
2. Set `standards: {mode: changed-lines}` in `.crewline/module.yaml`, so existing violations do not block new work; only lines a
   change touches do (STD-006). The checker's output has to name `path:line`; the commands above do.
3. Run the command through `crewline run` before IMPLEMENTATION_REVIEW, as for any checker.

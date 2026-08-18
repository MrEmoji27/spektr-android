# No workflows here, on purpose

This branch is a mirror. The tests, the release builds and everything else run
on the canonical repository:

  https://github.com/MrEmoji27/spektr

Two reasons they are not here. A mirror re-running the same suite proves
nothing the original has not already proved, and it burns Actions minutes to
do it. And the suite would fail anyway: this branch swaps the root README for
the port's, and three tests read README.md as the project's documentation —
they check that every offered mode appears in the mode table, that the opt-in
`(o)` variants are named, and that every `--flag` in `--help` is documented.
All three are correct about the file they are pointed at, and wrong about
which file this branch has.

That is worth stating rather than silencing: the tests are not broken, the
mirror is unusual, and it is the mirror that should absorb that.

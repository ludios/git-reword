<!-- clank-right
languages       = ["typescript"]
space_alignment = false
-->

# Project map

`git-reword` is the tool, a bash script whose header comment documents it. `tests/git_reword.test.ts` tests it.

The tests use `node:test` and `node:assert/strict` instead of `vitest`, so that this repository needs no `package.json` and no `node_modules`. Node strips the types when it runs the tests; nothing checks them.

# Before committing

	shellcheck git-reword
	node --test
	oxfmt --check tests/
	oxlint tests/

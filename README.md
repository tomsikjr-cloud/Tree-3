# TREE(3) — v0.11

A small tree-drawing puzzle inspired by Friedman's TREE(3). Build a sequence of colored rooted trees without letting an earlier tree embed inside a later one.

## Run

Download `index.html` and open it in a modern browser. No installation, build step, or server is needed.

All game logic and styling are in the HTML file. The game works offline; Google Fonts is optional and falls back to local fonts when unavailable.

## Play

1. Choose a color and click the canvas to plant a root.
2. Select a node, then click an empty spot to add a child, or use **+ Child** to add one and automatically arrange the tree.
3. On turn **n**, use between 1 and **n** nodes.
4. Press **Submit tree** to check your move against every accepted tree.

You lose if an earlier tree embeds in your new tree. Matching nodes must have the same colors, ancestry and branching must be preserved, and edges can stretch into paths. Sibling order and drawing position do not matter. The earlier root may match a node anywhere in the new tree.

For example, after submitting a single coral node as your first tree, any later tree containing coral loses.

## Controls and features

- Drag nodes to reposition them; **Arrange** automatically lays out the tree.
- **+ Child** spaces branches apart. Crowded click placements also trigger rearrangement.
- **Recolor** applies the chosen color to the selected node.
- **Delete** removes the selected node and its descendants.
- **Undo** or **Ctrl/Command + Z** reverses an edit.
- Failed submissions highlight the matching nodes and paths. Click a history card to inspect an earlier tree.
- **Restart** starts a fresh sequence. Browser storage remembers your current run and personal best when available.

## v0.11

Adds automatic spacing when children are added, overlap detection for click placements, and expanded drawing bounds for larger trees.

## Validation

The embedding checker was compared with an independent exhaustive checker on 13,924 small tree pairs, including verification of the highlighted mappings. Layout checks cover crowded siblings, deep branches, additions to higher nodes, and undo snapshots.

This is a playable sequence-building puzzle, not a calculation of the numerical value of TREE(3).


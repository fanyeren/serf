## 0.1.2 (Unreleased)

FEATURES:

  * Can now configure Serf with files or directories of files by specifying
    the `-config-file` and/or `-config-dir` flags to the agent.

IMPROVEMENTS:

  * Random staggering of periodic routines to avoid cluster-wide
    synchronization
  * Push/Pull timer automatically slows down as cluster grows to avoid
    congestion

BUG FIXES:

  * Nodes that previously left and rejoin won't get stuck in 'leaving' state.
    [GH-18]
  * Fixing alignment issues on i386 for atomic operations [GH-20]

## 0.1.1 (October 23, 2013)

BUG FIXES:

  * Default node name is outputted when "serf agent" is called with no args.
  * Remove node from reap list after join so a fast re-join doesn't lose the
    member.

## 0.1.0 (October 23, 2013)

* Initial release

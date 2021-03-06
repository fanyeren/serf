## 0.2.0 (Unreleased)

FEATURES:

  * Can now configure Serf with files or directories of files by specifying
    the `-config-file` and/or `-config-dir` flags to the agent.
  * New command `serf force-leave` can be used to force a "failed" node
    to the "left" state.
  * Serf now supports message encryption and verification so that it can
    be used on untrusted networks [GH-25]
  * The `-join` flag on `serf agent` can be used to join a cluster when
    starting an agent. [GH-42]

IMPROVEMENTS:

  * Random staggering of periodic routines to avoid cluster-wide
    synchronization
  * Push/Pull timer automatically slows down as cluster grows to avoid
    congestion
  * Messages are compressed to reduce bandwidth utilization
  * `serf members` now provides node roles in output

BUG FIXES:

  * Event handlers work on Windows now by executing commands through
    `cmd /C` [GH-37]
  * Nodes that previously left and rejoin won't get stuck in 'leaving' state.
    [GH-18]
  * Fixing alignment issues on i386 for atomic operations [GH-20]
  * "trace" log level works [GH-31]

## 0.1.1 (October 23, 2013)

BUG FIXES:

  * Default node name is outputted when "serf agent" is called with no args.
  * Remove node from reap list after join so a fast re-join doesn't lose the
    member.

## 0.1.0 (October 23, 2013)

* Initial release

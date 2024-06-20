# EBS Snapshots

Snapshots are what you'd think: a backup taken at a specific point in time.

It's not necessary to detach a volume to take a snapshot, but it IS recommended.

Can copy snapshots across AZs, which is how you "move" EBS between zones.

## EBS Snapshot Features

* EBS Snapshot Archive
    * Move a snapshot to an "archive tier" that is 75% cheaper.
    * Takes 24 to 72 hours to restore from archive.

* Recyle Bin for EBS Snapshots
    * An alternative to permanent deletion
    * Prevents accidental deletion
    * We're able to specify how long snapshots are stored in recycle, from 1 day to 1 year.

* Fast Snapshot Restore
    * Force full initialization of a snapshot.
    * No latency on first use
    * Expensive $$$
    
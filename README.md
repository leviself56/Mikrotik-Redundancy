# Mikrotik Redundancy
## Auto fail over to redundant link on link failure of primary interface

Add the script under `/system/script`
Be sure to modify the `primaryup` and `secondaryup` interfaces to match your naming schema.
Then add a scheduler to run every `1s` in `/system/scheduler`
The `ON-EVENT` should run your redundancy script like: `/system script run redundancy`

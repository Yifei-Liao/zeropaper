
## Background jobs

Never launch a long-running job with `nohup` or a detached `&` — it escapes harness tracking and stall detection. Use a harness-tracked background job instead (the Bash tool's `run_in_background`) so the job stays monitored and its output remains retrievable.

Make long jobs resumable: checkpoint/cache results to disk frequently and skip already-done work on restart, and log unbuffered in append mode (e.g. `python -u … >> log 2>&1`) so progress survives an interruption.

Write `rm -rf` targets as literal paths (`rm -rf output/stage3a/scratch/exhibits_i2`), never built from shell variables (`rm -rf $PWD/$S/x`). The runtime's safety check stops a variable-built `rm -rf` for human approval even in bypass mode, and in an unattended run nobody answers, so the pipeline sits idle until someone notices.

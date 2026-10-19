# Octop UI evidence — 2026-10-19

The screenshots show the actual, unmodified Dashboard components at the following PR heads, using local sample API fixtures in a browser. They do not represent a real LLM turn or a live-backend end-to-end test. Database and runtime claims rely on the separate regression tests documented in the PRs.

| PR | Source head | Scenario |
| --- | --- | --- |
| #1051 | `a107ef3b93563a32b94d0e20331dbdf7ff14024a` | Overscroll starts a history refresh. A newer local message update arrives before the delayed history response. The newer content remains after the stale response finishes. |
| #1054 | `2f4b868643ab2ff65b008562a11de7a4bf781ee0` | The conversation title menu exposes Export conversation. Clicking it calls the existing export endpoint and downloads `Deployment checklist-o-thread.json`; the downloaded sample payload has format `octop-history-v2` and two messages. |
| #1057 | `de9924c426500c85e9cbcc624a6d52635b7bddf8` | Archive sends `archived: true`; the thread appears in Archived. Restore sends `archived: false`; it returns to Current and the sample conversation remains visible. |

## Files

- `1051-refresh-in-flight.png`, `1051-newer-message-preserved.png`
- `1054-export-menu.png`, `1054-export-success.png`, `1054-sample-download.json`
- `1057-archive-menu.png`, `1057-archived-view.png`, `1057-restore-menu.png`, `1057-restored-current-view.png`

Only sample users, messages and model labels are used; no service credentials or personal conversation history are included.

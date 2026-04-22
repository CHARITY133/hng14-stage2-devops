Fix 1
File: worker/worker.py
Issue: Redis connection used localhost which fails in Docker
Fix: Changed host to "redis" to match docker-compose service name

Fix 2
File: api/main.py
Issue: Unused import (os) caused lint failure
Fix: Removed unused import

Fix 3
File: worker/worker.py
Issue: Missing newline at end of file (W292)
Fix: Added newline at end

Fix 4
File: worker/worker.py
Issue: Incorrect spacing (E302)
Fix: Added required blank lines between functions

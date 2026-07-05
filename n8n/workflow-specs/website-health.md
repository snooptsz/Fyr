# n8n Workflow Spec - Website Health Check

## Purpose
Check whether the public beta is reachable and the main flows are not obviously broken.

## Trigger
Schedule every 6 hours.

## URLs to check

- Home page
- Login page
- Signup page
- Communities page
- Contributor page
- Contact page

## Nodes

1. Schedule trigger.
2. HTTP Request for each URL.
3. IF status code is not 200/2xx, mark as failed.
4. GitHub create issue for critical failures.
5. Notify founder.

## Output

- Checked URL
- Status code
- Failure reason
- Suggested priority

## Safety

This workflow performs non-invasive availability checks only.

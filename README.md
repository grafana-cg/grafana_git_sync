# grafana_git_sync

Git Sync in Grafana lets you manage your dashboards as code as JSON files stored in GitHub. You and your team can version control, collaborate, and automate deployments efficiently.

Using Git Sync, you can:

Manage dashboard configuration outside of Grafana instances using Git
Introduce a review process for creating and modifying dashboards
Replicate dashboards across multiple instances

Provisioning folder
Git Sync creates a folder for all the synchronized resources to live under. You can continue to have unprovisioned resources outside that folder.

Make changes in Grafana
Whenever you modify a dashboard directly from the UI, Grafana can commit changes to Git upon saving. You can configure settings to either enforce PR approvals before merging in your repository, or allow direct commits.

Grafana periodically polls GitHub at a regular internal to synchronize any changes. The default polling interval is 60 seconds, and you can change this setting in the Grafana UI.

If you enable the webhooks feature, repository notifications appear almost immediately.
Without webhooks, Grafana polls for changes at the specified interval.
Make changes in your GitHub repositories
With Git Sync, you can make changes to the files in the provisioned folder in GitHub and see them in Grafana. Automated workflows ensure those changes are automatically represented in the Grafana database by updating Git. The Grafana UI reads the database and updates the UI to reflect these changes.

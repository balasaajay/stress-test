# stress-test
Ansible playbook to stress test a server for any hardware errors

## Commands to run the playbook:

### Add the host to hosts file (if not already present).

### To start stress-ng tests on a host:
``` ansible-playbook stress.yml -K -e 'target=<hostname> --tags=run-stress -i hosts ```

### To stop stress-ng tests:
#### Stress tests run for 4 hours by default, if yoy want to stop tests anytime before 4hrs, use this.
``` ansible-playbook stress.yml -K -e 'target=<hostname> --tags=stop-stress -i hosts ```

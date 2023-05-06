<p align="left"><img src="https://www.versio.io/img/supported-technology/hetzner-cloud.svg"></p
<h1>Hetzner runner deployments</h1>

## Usage

```yaml
- name: Enable Hetzner Virtual Servers
  uses: armbian/actions/hetzner@main
  with:
    action-type: enable # enable or disable VM cluster
    machine-type: cax21|cax31|... # server type
    machine-id: 0,1,2 ... # selected server
    runners-count: 1,2,3 # runners per server
    machine-count: 1,2,3 # numbers of servers
    key: ${{ secrets.KEY_TORRENTS }} # key which we have in the Hetzner API
    known_hosts: ${{ secrets.KNOWN_HOSTS_TORRENTS }}  # key_knowns_hosts which we have in the Hetzner API
    hetzner_id: ${{ secrets.HETZNER_ONE }} # Hetzner API token
    github_token: ${{ secrets.ACCESS_TOKEN }} # Github action token

```

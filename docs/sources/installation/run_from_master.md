page_title: Run Grafana-Zabbix from master
page_description: Building instructions for Grafana-Zabbix.

# Run from master
If you want to build a package yourself, or contribute - here is a guide for how to do that.

### Dependencies

- NodeJS LTS

### Enter into zabbix plugin dir

```bash
cd /var/lib/grafana/plugins/alexanderzobnin-zabbix-app
```

### Building plugin
**Centos**
complete yarn how to:https://yarnpkg.com/lang/en/docs/install/#centos-stable
short yarn how to:
```bash
curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
yum install yarn
yarn install --pure-lockfile
yarn build
```

or 

```bash
npm install -g yarn
yarn install --pure-lockfile
yarn build
```

### To build plugin and rebuild on file change

```bash
yarn watch
```

### Run tests
```bash
yarn test
```

### Run tests on file change
```bash
yarn jest
```

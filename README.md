# Cataclysm-BN translations

Hosts Cataclysm-BN `.po` files under `lang/po/<lang>.po`, matching the old Cataclysm-BN layout.

Translations are updated either from Transifex or from Cataclysm-BN release workflow artifacts.

Required repository secret:

- `TX_TOKEN`: Transifex API token.

## Pull locally with Transifex CLI

From this repository:

```sh
curl -sL https://github.com/transifex/cli/releases/download/v1.6.17/tx-linux-amd64.tar.gz | sudo tar zxvf - -C /usr/local/bin tx
export TX_TOKEN=your-transifex-token
mkdir -p lang/po
tx pull --force --all
find lang/po -maxdepth 1 -type f -name '*.po' | sort
git status --short -- lang/po
```

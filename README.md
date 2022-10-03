# Nexo Pro API Wrapper built with Python

- ✨ Work in Progress
- 🎌 Built with Python
- 🐋 Docker Available
- 🍻 Actively Maintained

## Description 📰

This is an unofficial Python wrapper for the Nexo Pro exchange REST API v1. I am in no way affiliated with Nexo, use at your own risk.

If you came here looking for the Nexo exchange to purchase cryptocurrencies, then go here. If you want to automate interactions with Nexo, stick around.

Heavily influenced by (https://github.com/sammchardy/python-binance)[python-binance]

## Roadmap 🌱

See it on Issue https://github.com/guilyx/python-nexo/issues/1

## Preparation 🔎

- Register a Nexo Account.
- Generate an API Key in Nexo Pro with the permissions you want.

## Set it up 💾

### PIP

1. Install the pip package: `python3 -m pip install python-nexo`
2. Explore the API:

```python3
import nexo
import os
c = nexo.Client("your_api_key", "your_api_secret")
balances = c.get_account_balances()
print(balances)
```

### Docker (source)

1. Clone the Project: `git clone -b master https://github.com/guilyx/python-nexo.git`
2. Move to the Repository: `cd python-nexo`
3. Create a copy of `.env.example` and name it `.env`
4. Fill up your API Key/Secret
5. Build and Compose the Docker: `docker-compose -f docker/docker-compose.yml up` - The container should keep running so that you can explore the API
6. Attach to the docker: `docker exec -it $(docker ps -qf "name=docker_python-nexo") /bin/bash`
7. Run python in the docker's bash environment: `python3`
8. From there, copy the following snippet to instantiate a Client:

```python3
import nexo
import os
nexo_key = os.getenv("NEXO_PUBLIC_KEY")
nexo_secret = os.getenv("NEXO_SECRET_KEY")
assert(nexo_key)
assert(nexo_secret)
c = nexo.Client(nexo_key, nexo_secret)
```

9. You can now explore the client's exposed endpoints, for instance:

```python3
balances = c.get_account_balances()
print(balances)
```

## Contribute 🆘

Open an issue to state clearly the contribution you want to make. Upon aproval send in a PR with the Issue referenced. (Implement Issue #No / Fix Issue #No).

## Maintainers Ⓜ️

- Erwin Lejeune

## Buy me a Coffee

*ERC-20 / EVM: **0x482A82761710aeAf04665BB28E32Fb256B4a7bC8***

*BTC: **bc1q0c45w3jvlwclvuv9axlwq4sfu2kqy4w9xx225j***

*DOT: **1Nt7G2igCuvYrfuD2Y3mCkFaU4iLS9AZytyVgZ5VBUKktjX***

*DAG: **DAG7rGLbD71VrU6nWPrepdzcyRS6rFVvfWjwRKg5***

*LUNC: terra12n3xscq5efr7mfd6pk5ehtlsgmaazlezhypa7g***

# PyProxies

**PyProxies** is a Python project for fetching free proxies and estimating their performance locally.

**Note:** These proxies may not deliver the best performance nor the best privacy and that this is more of a study/prototype project.

*Actually good* proxies, which also most likely *don't* sell one's data, can generally not publically be found for free, though some sites like [Webshare](https://www.webshare.io) may offer free trials or something similar with more trustworthy proxies (with certain restrictions such as bandwith limitations).

## Installation and Usage

1. Clone the git repository
```shell
git clone https://github.com/DarthRevan333/PyProxies
```

2. Install dependencies (also listed [here](requirements.txt))
   ```shell
   pip install requests
   ```

3. Use the cloned project

    - Run the main script directly
        ```shell
        python PyProxies
        ```

      This will take some time and then display all found proxies

    - Use it in other Python scripts
        ```Python
        from PyProxies import load_proxies_list

        if __name__ == "__main__":
            # This example is a simplified version of the main script
            pl = load_proxies_list()
            print("\n".join([f"{p.protocol}://{p.ip}" for p in pl.get_n_best(20)]))
        ```

        Note that you can only import from the [inner PyProxies folder](PyProxies) containing the [\_\_init\_\_.py](PyProxies/__init__.py) , but run both

## Sources

This project relies on the free [Proxyscrape API](https://docs.proxyscrape.com) for fetching free proxies and on randomly chosen more or less well known [Websites](PyProxies/test_urls.py) for testing these free proxies.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

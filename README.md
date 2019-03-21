# regist
`regist` is a command line tool, intended to execute remote scripts from your gists on any local machine. It downloads and caches the scripts from your [https://gist.github.com](https://gist.github.com). To start using `regist` you need to set some environment variables:
- `REGIST_TOKEN` is your github token to access your gists.
- `REGIST_GIST_ID` is your gist id, that contains bash scripts.
- `REGIST_CACHE_DIR` is cache directory (`~/.regist` by default).
- `REGIST_MAX_TIME` is cache expiration time (`3600 * 24 * 10` by default).

To execute remote script type:
```sh
# As current user
regist hello_world arg1 arg2
# As root
sudo -E regist hello_world arg1 arg2
```
Make sure you've created a file `hello_world.sh` within your gist.

Some additional commands are available:
```sh
# Print help information
regist --help
# Print version
regist --version
# Remove cache dir
regist --reset
# Force downloading the script
regist --update hello_world 123
```

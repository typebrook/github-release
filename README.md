# GitHub Action for uploading release asset with curl

Use a simple shell script to upload a file to an existing Github release, fork from [wei/curl](https://github.com/wei/curl).<br>
Original idea comes from script by [stefanbuck](https://gist.github.com/stefanbuck/ce788fee19ab6eb0b4447a85fc99f447).


## Usage

### GitHub Actions
```
on: push
jobs:
  upload-release-asset:
    runs-on: ubuntu-latest
    steps:
      - name: Upload file to Release Asset
        uses: typebrook/upload-release-asset@v1
        env:
          github_api_token: ${{ secrets.GITHUB_TOKEN  }}
          owner: typebrook
          repo: upload-release-asset
          tag: ${{ github.ref }}
          filename: foo
          overwrite: true
```


## Author
[typebrook](https://github.com/typebrook)@gmail.com


## License
[MIT](https://opensource.org/licenses/mit-license.php)

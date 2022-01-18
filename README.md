# rimgo-quay

A [rimgo](https://codeberg.org/video-prize-ranch/rimgo) image, on Quay.

[Quay page](https://quay.io/repository/pussthecatorg/rimgo) | [GitHub page](https://github.com/PussTheCat-org/rimgo-quay)

This image mostly exist for the [PussTheCat.org](https://pussthecat.org/) [instance](https://rimgo.pussthecat.org/), but others are free to use it.

## Usage:

- Download (or copy the content of) the `docker-compose.yml` 
- Download (or copy the content of) the `config.yml` from this repository, or from upstream: https://codeberg.org/video-prize-ranch/rimgo/src/branch/main/config.yml
- Customize the `config.yml` file how you want
- Move both files to the folder you want
- `docker-compose up -d`

## Credit:

- The Invidious `container-release.yml` file: https://github.com/iv-org/invidious/blob/master/.github/workflows/container-release.yml
- [@unixfox](https://github.com/unixfox), invidious-custom `docker-image.yml` file: https://github.com/unixfox/invidious-custom/blob/master/.github/workflows

# setup-sdl2-frameworks

![CI](https://github.com/BrettDong/setup-sdl2-frameworks/actions/workflows/test.yml/badge.svg) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A GitHub Action to download and install SDL2 frameworks on macOS runners from [libsdl-org](https://github.com/libsdl-org/) GitHub repositories.

## Usage

Example usage:
```yml
      - name: Setup SDL2 frameworks
        uses: BrettDong/setup-sdl2-frameworks@main
        with:
          sdl2: latest
          sdl2-ttf: latest
          sdl2-image: 2.6.3
          sdl2-mixer: none
```

## Inputs

| Name | Description | Default
|---|---|---|
| `token` | A GitHub token for retrieving SDL2 releases information throught GitHub API | `GITHUB_TOKEN` |
| `dest` | Destination folder where SDL2 frameworks will be installed to | `/Users/runner/Library/Frameworks` |
| `sdl2` | SDL2 version to be installed | `latest` |
| `sdl2-ttf` | SDL2_ttf version to be installed | `none` |
| `sdl2-image` | SDL2_image version to be installed | `none` |
| `sdl2-mixer` | SDL2_mixer version to be installed | `none` |

Version of an SDL2 component can be specified by

| Value | Description |
|---|---|
| `latest` | Latest release available on GitHub |
| `2.6.3` | A specific version |
| `none` | Do not install this component |

## Credits

This is developed on top of the template [typescript-action](https://github.com/actions/typescript-action).

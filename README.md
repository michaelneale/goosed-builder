# Goosed Builder

This repository automatically builds `goosed` binaries from the [block/goose](https://github.com/block/goose) main branch and publishes them as releases.

## How It Works

A GitHub Actions workflow runs daily at 2 AM UTC (or can be triggered manually) that:

1. Fetches the latest code from `block/goose` main branch
2. Builds `goosed` binaries for multiple platforms:
   - macOS Intel (x86_64)
   - macOS Apple Silicon (ARM64)
   - Linux Intel/AMD (x86_64)
   - Linux ARM64
3. Creates/updates a "latest" release with all binaries

## Download

Get the latest binaries from the [Releases page](../../releases/latest).

### Quick Install

```bash
# macOS Apple Silicon (ARM64)
curl -L -o goosed https://github.com/michaelneale/goosed-builder/releases/download/latest/goosed-macos-aarch64
chmod +x goosed
./goosed

# macOS Intel (x86_64)
curl -L -o goosed https://github.com/michaelneale/goosed-builder/releases/download/latest/goosed-macos-x86_64
chmod +x goosed
./goosed

# Linux x86_64
curl -L -o goosed https://github.com/michaelneale/goosed-builder/releases/download/latest/goosed-linux-x86_64
chmod +x goosed
./goosed

# Linux ARM64
curl -L -o goosed https://github.com/michaelneale/goosed-builder/releases/download/latest/goosed-linux-aarch64
chmod +x goosed
./goosed
```

## Manual Trigger

You can manually trigger a build by going to the [Actions tab](../../actions/workflows/build-and-release.yml) and clicking "Run workflow".

# Python

This is a Python engine for developing python apps on [Microbox](http://microbox.cloud).

## Usage
To use the Python engine, specify `python` as your `engine` in your boxfile.yml

```yaml
run.config:
  engine: python
```

## Configuration Options
This engine exposes configuration options through the [boxfile.yml](https://docs.microbox.cloud/boxfile/), a yaml config file used to provision and configure your app's infrastructure when using Microbox.

### Python Settings
The following setting allows you to define your Python runtime environment.

#### runtime
Specifies which Python runtime and version to use. The following runtimes are available:

- python-2.7
- python-3.4
- python-3.5
- python-3.6

```yaml
run.config:
  engine.config:
    runtime: python-3.5
```

#### pip_install
Allows for a custom user-defined pip install command.

note: The custom pip install command should always include `-I` to ensure the binaries get copied on each build.

```yaml
run.config:
  engine.config:
    pip_install: 'pip install --index-url https://my.custom.index -r requirements/private.txt -I'
```

## Help & Support
This is a Python engine provided by [Microbox](http://microbox.cloud). If you need help with this engine, you can reach out to us in the [Microbox Discord](https://discord.gg/MCDdHfy). If you are running into an issue with the engine, feel free to [create a new issue on this project](https://github.com/mu-box/microbox-engine-python/issues/new).

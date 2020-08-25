# PHP Android CLI

PHP Android CLI create/generate MicroApp Android-Studio Gradle project with:

  - Modules as MicroApp (application/library)
  - MicroApp project & application/library level `build.gradle` with package name & `dimensions` & `variants`
  - Manage `settings.gradle`
  - Generate `manifest` file & `res` with default `icon`, `color`, `style` & `values`
  - ...more

# New Features!

  - ...


You can also:
  - set `targetSdk`
  - set `buildToolsVersion`
  - set `minSdk` & `maxSdk`

### Tech

PHP Android CLI uses:

* [Symfony Console](https://symfony.com/console) - ...

### Installation

PHP Android CLI requires [PHP](https://php.net/) v5+ to run.

Just download the [`harmonyandroid`](https://github.com/karthee-ui/AndroidCli/blob/master/harmonyandroid.phar).

Install Phar file - Mac/Linux
```sh
$ chmod +x harmonyandroid.phar
$ sudo mv harmonyandroid.phar /usr/local/bin/harmonyandroid
$ harmonyandroid --version
```

Install Phar file - Windows
- Put all your .phar files to one directory like C:\php\phars
- Add C:\php\phars to system environment variables (right-click my Computer -> Properties -> Advanced System Settings -> Environment variables)
- Start the command prompt (find command prompt in start menu then right-click and select Run as Administrator)
- Type the following commands
```sh
$ echo @php "%~dp0harmonyandroid.phar" %*>harmonyandroid.bat
$ harmonyandroid --version
```

## USAGE

### Syntax
```sh
$ harmonyandroid create <PROJECT_NAME> <PACKAGE> [OPTIONS]
```

### Basic use

Create `HelloWorld` project with `com.example.helloworld` package name:
```sh
harmonyandroid create HelloWorld com.example.helloworld
```

### Create `Modules` along with `App`
Create `HelloWorld` project with `sdk` library & `admin` application
```sh
harmonyandroid create HelloWorld com.example.helloworld --modules=sdk:library,admin
```

### Create `productVariants`: `free` & `paid` variant
```sh
harmonyandroid create HelloWorld com.example.helloworld --variants=free:type,paid:type
```

here `type` is the `dimension`

## Options
### Default
PHP Android CLI is currently using default values for latest Android. These are:

| OPTIONS | Usage | DEFAULT |
| ------ | ------ | ------ |
| `--compileSdk`/`-cs` | set `targetSdk` | 29 |
| `--buildTools`/`-bt` | set `buildToolsVersion` | 29.0.1 |
| `--minSdk`/`-ms` | set `minSdk` | 16 |
| `--targetSdk`/`-ts` | set `maxSdk` | 29 |
| `--androidX`/`-x` | Enable/Disable AndroidX | true |
| `--jetifier`/`-j` | Enable/Disable Jetifier | true |

Use `--force` to re-write existing project.

### Todos
---

License
----

MIT


**Free Software, Hell Yeah!**

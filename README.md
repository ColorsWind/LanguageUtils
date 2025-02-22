# If you are looking for LanguageUtils that works with version 1.19.4+, please try [LanguageUtilsPlus](https://github.com/ColorsWind/LanguageUtilsPlus), which is 100% API compatible.


Language Utils
==============

[![Build Status](https://ci.nyaacat.com/job/LanguageUtils/badge/icon)](https://ci.nyaacat.com/job/LanguageUtils/)

A Bukkit/Spigot API offering the ability to get the name of **vanilla** items, entities, enchantments, and enchantment levels.

The major version of this API supports 1.12. If you are using 1.7.10, 1.8.9, 1.9.4, 1.10.2, or 1.11.2, please download `1.4.0` version for 1.7.10(with suffix `-1.7.10`) or `1.4.0` for 1.8.9(no suffix), `1.5.x` for 1.9.4, or `1.6.x` for 1.10.2, `1.8.x` for 1.11.2 accordingly.

Version `2.1.x` are for 1.13, `2.2.x` are for 1.14, `2.3.x` are for 1.15 and `2.4.x` are for 1.16.

Loading language files may cost 100-300 ms, but it should be fine to wait, and you can even disable the loading of any language.

Also, if you want to know how to add customized language entries, just read the `README.txt` inside `lang/` folder.

You can get the latest build [here](https://ci.nyaacat.com/job/LanguageUtils/).
You can find old builds from the [original author's Release Page](https://github.com/MascusJeoraly/LanguageUtils/releases)
or [our release page](https://github.com/NyaaCat/LanguageUtils/releases).

You CAN install this plugin on Cauldron/KCauldron servers if you are using 1.2.0.1-1.7.10+ version of this plugin. Again, the API only supports **vanilla** language entries. It will just return the auto-generated material name of an item in mods.

## Configuration

```
# When a name in the language requested does not exist, the name will be retrieved in this language. The default fall back language is English.
FallbackLanguage=en_us
# If you want to enable the loading of a language, add it to the following list
LoadLanguage= [en_us, zh_cn, zh_tw]
# Or
LoadLanguage:
- en_us
- zh_cn
- zh_tw
# If you want to load all the languages, add "all" to the list:
LoadLanguage:
- all
```

## Use Language Utils

You can also see this [Example](https://github.com/MascusJeoraly/LangUtilsExample "Example") for detailed usage.

### Plugin dependency

First, you need to add LangUtils as a dependency in your `plugin.yml` file:

	depend: [LangUtils]

If you have multiple dependencies, add `,` between each of them:

	depend: [LangUtils, Vault]

Instead of adding LangUtils as a dependency, you can just add it as a soft dependency:

	softdepend: [LangUtils]

### Build Path

Just add this library to your build path.

### Maven/Gradle dependency

This plugin is currently hosted on NyaaCommunity's [CI server](https://ci.nyaacat.com/maven/com/meowj/LangUtils/).

If you are using Gradle, add the following to you `build.gradle`:

	repositories {
	    maven {
	        url 'https://ci.nyaacat.com/maven/'
	    }
	}
	dependencies {
		compile group: 'com.meowj', name: 'LangUtils', version: '2.3-SNAPSHOT' // Please check the latest version
	}

If you are using Maven, add the following to your `pom.xml`:

	<repositories>
	  <repository>
	    <id>lang-utils-repo</id>
	    <url>https://ci.nyaacat.com/maven/</url>
	  </repository>
	</repository>

	<dependencies>
	  <dependency>
	    <groupId>com.meowj</groupId>
	    <artifactId>LangUtils</artifactId>
		<!--Please check the latest version -->  
	    <version>2.3-SNAPSHOT</version>
	  </dependency>
	</dependencies>

### Usage

For further information, see the [Example](https://github.com/MascusJeoraly/LangUtilsExample "Example") plugin or `LanguageHelper` and `LocaleHelper`.

----------

## Contribute to this Project

If you don't have [Gradle](http://gradle.org/ "Gradle") installed, you can download one or use `gradlew`(Windows) / `./gradlew`(Linux) instead of `gradle` in the commands.

If you don't have permission when using `./gradlew`, run `chmod +x gradlew` and run the command again.

### Setup Dev Environment

If you are using IntelliJ IDEA(recommended), just import the `build.gradle` file. IntelliJ should automatically handle the dependencies.

If you just want to create a Module instead of a Project, run `gradle ideaModule` instead, or just directly import `build.gradle` file to IntelliJ.

If you are using Eclipse(not tested)

	[Navigate to the project directory]
	$ gradle eclipse

### Pull Request

If you find any problems or want to improve the efficiency, please send me PR or issues.

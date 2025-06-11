# Development

How to get the docs up and running locally

**Install Ruby Installer**
Download RubyInstaller for Windows:

https://rubyinstaller.org/

Choose the latest Ruby+Devkit version (e.g., Ruby 3.2.x).

Run the Installer

During installation:

    Check "Add Ruby executables to your PATH"
    Check "Run 'ridk install' after setup"

Install DevKit (important for native gems like ffi)

After setup, a command window will open. Select:

    Option: MSYS2 and MINGW development toolchain

**Run**

```
cd documentation

bundle install

```

Then:

```
bundle exec jekyll serve --source . --destination ../_site
```

or 

```
bundle exec jekyll serve --livereload --drafts --trace --source . --destination ../_site
```
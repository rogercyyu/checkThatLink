# checkThatLink

This is a CLI tool used to check an html file for the status of the URL's it contains.

The application requires the path to a file as it's first positional argument.

```$  checkThatLink.py [fileName]```

The status of the URL will be shown by colour
  - Green = good link
  - Cyan = secured link
  - Red = bad link
  - Grey = unknown link
  
### Options

You can also use the optional flag argument -s or --secureHttp to indicate that you want to see if the supplied http URL's
will work using https instead.

``` $  checkThatLink.py [fileName] -s```

You can choose to have the output be in JSON format instead of the original output by using the -j or --json flags.

``` $  checkThatLink.py [fileName] -j```

There is also the option to get only good, or bad matches with the corresponding flags: 

``` $  checkThatLink.py [fileName] --good OR --bad```

The optional flag argument -i or --ignore with a filepath will load and parse an ignored URLs text file.

``` $  checkThatLink.py [fileName] -i [ignoreFile]```

The format of an ignored URLs text file is as follows:
- URLs must be placed on separate lines and begin with either `http` or `https`
- Any line that begins with `#` is a comment and will not be parsed

To check the status of the 10 latest Telescope posts you can use the -t --telescope optional argument.
Doing so will ignore the file given and instead check Telescope.

*You must have Telescope's backend running locally in order to use this feature*

``` $  checkThatLink.py [fileName] -t```


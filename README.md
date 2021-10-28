# Gist Fetch

Query github gists for a user and display new gists since last run.

## Description

By default, this script does what the short description says. However, there are several command
line switches that provide extra functionality. A user can then display all gists for a github user,
and/or display deleted gists for that user. There is also an option to check the rate limit 
values for the session - unauthenticated github gist queries are limited to 60 per hour.

        usage: gist_fetch [-h] [-p] [-d] [-r] username
        
        positional arguments:
          username         github username - required
        
        optional arguments:
          -h, --help       show this help message and exit
          -p, --print_all  dont just print new gists
          -d, --deleted    also show deleted gists
          -r, --rate       check current rate limits and exit


## Getting Started

### Dependencies

I am expecting a modern linux distribution which comes with python3 (as python2 is deprecated)
and has pip3 installed, or the ability to do so. 

requirements.txt lists additional python libraries which we will install for the user

```
requests~=2.10
argparse~=1.1
```
### Installing

In the code directory, execute:

    ./setup

This will install the two python3 libraries as detailed in the dependencies section.

### Executing program

To execute, in the code directory (username is a required parameter):

    ./gist_fetch github_username

For command line switches:

    ./gist_fetch --help

Example:

    ./gist_fetch --print_all --deleted github_username

## Help

There is a rate limit of 60 requests per hour when unauthenticated, 
so use ./gist_fetch github_username --rate to check your request values.

The API limits 3000 results - if a user has more gists, they will not 
all be returned.

For further help, execute:
```
./gist_fetch --help
```

## Authors

Contributors names and contact info

Anonymous Contributor
ex. [@anon](https://twitter.com/no_one_here)

## Version History

* 0.1
    * Initial Release

## License

This project is licensed under the NO_LICENSE License - see the LICENSE.md file for details

## Acknowledgments

Coffee

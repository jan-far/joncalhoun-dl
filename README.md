# joncalhoun-dl 🔥⬇

Downloads Go tutorial videos from <https://courses.calhoun.io>

> **Before you proceed, note that you must be a paid user for the paid content to download**

Kindly create your account [here](https://courses.calhoun.io/signup?). Jon is a great teacher, consider buying his premium courses if you want to.

## How to use

+ Ensure [youtube-dl](https://github.com/ytdl-org/youtube-dl#installation) is installed and in your PATH.
+ Run the following commands

```bash
    $ git clone git@github.com:timolinn/joncalhoun-dl.git
    $ cd joncalhoun-dl
    $ go run main.go --email=jon@doe.com --password=12345 --course=gophercises
     [courses.calhoun.io]: fetching video urls for gophercises
     [courses.calhoun.io]: fetching data from https://courses.calhoun.io/courses/cor_gophercises...
```

Video downloads **resumes** from where it stopped, so should you experience network interruption nothing to worry about just make sure the output directory remains the same.

### Command [OPTIONS]

+ `--email` : Your account email address. Sign up [here](https://courses.calhoun.io/signup?)
+ `--password` : Your account password. _Unlike the unix password prompt, this will not hide your password by default, you'll have to keep an eye over your shoulder 😉_
+ `--course` : This is the name of the course you want to download. **Defaults** to `"gophercises"`
+ `--output` : Output directory (where the videos would be saved). **Defaults** to `"./videos/[course]"`

### Supported courses

+ [x] [gophercises](https://courses.calhoun.io/courses/cor_gophercises)
+ [x] [testwithgo](https://courses.calhoun.io/courses/cor_test)
+ [x] [webdevwithgo](https://courses.calhoun.io/courses/cor_webdev)
+ [ ] [advancedwebdevwithgo](https://https://courses.calhoun.io/courses/cor_awd)
+ [ ] [algorithms](https://courses.calhoun.io/courses/cor_algo)

### Nuance

Downloaded course videos would be automatically grouped inside `course directories` named after their respective courses titles e.g. `testwithgo` etc., without your input. These newly created `course directories` would be in a root directory named `videos` - which is also created at runtime.

### Contributing

There is still a couple features to implement, check the TODO list below and send a pull request.

### Tests

```bash
    $ go test
```

## TODO

+ [x] Add caching for requests
+ [x] Add default output directory
+ [x] Add output directoy flag
+ [ ] Add more unit tests
+ [ ] provide packaged release and semver
+ [ ] check for authentication error
+ [ ] prevent signin when using cache
+ [ ] choose video quality

### Authors

+ Timothy Onyiuke _([twitter](https://twitter.com/timolinn_))_

If you find this repository to be of any help, please consider giving it Star! 🔥

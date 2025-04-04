# NEW CODE IN WIP

We are refactoring the project to Symfony 5.4 to get the latest LTS, and we will use React for the Front.

First progress are on the UI/UX, you can check the Work in Progress here:
https://www.figma.com/proto/qyn8R2l52arJ34B5Lryvkb/lexiques?node-id=1%3A2&scaling=scale-down&page-id=0%3A1&starting-point-node-id=1%3A2

Any feedback is welcome.
# OLD CODE:

# Project 3 - Starter Kit - Symfony 5.*

## Presentation

This starter kit is here to easily start a repository for Wild Code School students.

It's symfony website-skeleton project with some additional library (webpack, fixtures) and tools to validate code standards.

* GrumPHP, as pre-commit hook, will run 2 tools when `git commit` is run :

  * PHP_CodeSniffer to check PSR12
  * PHPStan focuses on finding errors in your code (without actually running it)
  * PHPmd will check if you follow PHP best practices

  If tests fail, the commit is canceled and a warning message is displayed to developper.

* Github Action as Continuous Integration will be run when a branch with active pull request is updated on github. It will run :

  * Tasks to check if vendor, .idea, env.local are not versionned,
  * PHP_CodeSniffer, PHPStan and PHPmd with same configuration as GrumPHP.

## Getting Started for Students

### Prerequisites

Needed for the searchbar:
1. pdo_sqlite extension active in Laragon (Right click in Laragon window, PHP => Extension for the list)
2. sqlite extension active in Laragon

# Strikeout steps are NOT necessary

1. Check composer is installed
   <s>
2. Check yarn & node are installed
   </s>

### Install

1. Clone this project
2. Copy .env file in root to make your own .env.local
3. Run `composer install`
4. Create the database with this command: <br> php bin\console doctrine:database:create
5. Then the database tables with this command: <br> php bin\console doctrine:migrations:migrate
6. Build an index with the following url once you saved some Words to have the index for the Search feature work: <br> localhost:port/generate-index
   <s>
7. Run `yarn install`
8. Run `yarn encore dev` to build assets
   </s>

### Working

1. Run `symfony server:start` to launch your local php web server
   <s>
2. Run `yarn run dev --watch` to launch your local server for assets
   </s>
### Testing

1. Run `php ./vendor/bin/phpcs` to launch PHP code sniffer
2. Run `php ./vendor/bin/phpstan analyse src --level max` to launch PHPStan
3. Run `php ./vendor/bin/phpmd src text phpmd.xml` to launch PHP Mess Detector
3. Run `./node_modules/.bin/eslint assets/js` to launch ESLint JS linter
3. Run `../node_modules/.bin/sass-lint -c sass-linter.yml -v` to launch Sass-lint SASS/CSS linter

### Windows Users

If you develop on Windows, you should edit you git configuration to change your end of line rules with this command :

`git config --global core.autocrlf true`

## Deployment

Some files are used to manage automatic deployments (using tools as Caprover, Docker and Github Action). Please do not modify them.

* [captain-definition](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/captain-definition) Caprover entry point
* [Dockerfile](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/Dockerfile) Web app configuration for Docker container
* [docker-compose.yml](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/docker-compose.yml) ...not use it's used 😅
* [docker-entry.sh](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/docker-entry.sh) shell instruction to execute when docker image is built
* [nginx.conf](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/nginx.conf) Nginx server configuration
* [php.ini](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/php.ini) Php configuration


## Built With

* [Symfony](https://github.com/symfony/symfony)
* [GrumPHP](https://github.com/phpro/grumphp)
* [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
* [PHPStan](https://github.com/phpstan/phpstan)
* [PHPMD](http://phpmd.org)
* [ESLint](https://eslint.org/)
* [Sass-Lint](https://github.com/sasstools/sass-lint)



## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning


## Authors

Wild Code School trainers team

## License

MIT License

Copyright (c) 2019 aurelien@wildcodeschool.fr

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Acknowledgments


# 0.1.0 (2024-05-01)


### Bug Fixes

* **changelog:** checkout and use custom username and email ([e1ae0f7](https://github.com/99linesofcode/.github/commit/e1ae0f791d0fa3739099661a6590c84a3c7fb3b5))
* **changelog:** invalid workflow file ([7c24295](https://github.com/99linesofcode/.github/commit/7c2429595de24c34a9b56d602f43c56a4a4fe1fa))
* **changelog:** skip creating version file ([c610a21](https://github.com/99linesofcode/.github/commit/c610a213ea7a11b6e0793cd6786a613f6f2449f9))
* **dependabot:** config was in the wrong directory ([bf9ec76](https://github.com/99linesofcode/.github/commit/bf9ec761211e9daff67c26aef838ef2ad7c2b51e))
* **deploy:** align PHP version with (dev) containers ([c1843ff](https://github.com/99linesofcode/.github/commit/c1843ff2c09f186341dea21e7873574d1bb4ff92))
* **deploy:** cannot reference services context from global variables ([4fb8d27](https://github.com/99linesofcode/.github/commit/4fb8d27a8a61843edb0e22292ea403ec85f3f77f))
* **deploy:** deploy.yml was renamed to kamal.yml ([21b13e6](https://github.com/99linesofcode/.github/commit/21b13e6de48df8da5a2ee997d2476f9a8a0aa1ef))
* **deploy:** generate autoload.php and disable interaction ([815bf1d](https://github.com/99linesofcode/.github/commit/815bf1d9ad9e4c0e51a3ed9a77fa147cd47dfa5f))
* **deploy:** install composer and laravel dependencies ([c99f114](https://github.com/99linesofcode/.github/commit/c99f114ecbc50721b60194e402718338fdcafbc5))
* **deploy:** reduce number of tests for now ([655dc3e](https://github.com/99linesofcode/.github/commit/655dc3eeef125946a433862e37c625116945f7a7))
* **deploy:** should run on workflow call ([fcdfb3d](https://github.com/99linesofcode/.github/commit/fcdfb3d996b583e4b9c79d503e13af769d2b0ddf))
* **deploy:** typo prevented bundler from caching installed gems ([9237184](https://github.com/99linesofcode/.github/commit/923718419fc1cec11d6f7dd752243de83f46fc45))
* **deploy:** use correct syntax for defining env variables ([5628e02](https://github.com/99linesofcode/.github/commit/5628e02420ab4272ce04742fe392e385168f0d93))
* **test:** build tailwindcss manifest file so tests run succesfully ([dfacff5](https://github.com/99linesofcode/.github/commit/dfacff56bc5741222b8964572de150564010f4ae))
* **test:** copy .env.testing and set application encryption key ([577f716](https://github.com/99linesofcode/.github/commit/577f716ab8dc2b615388a0540df33cbb72f6d45d))
* **test:** run migrations in testing environment ([80b341e](https://github.com/99linesofcode/.github/commit/80b341ea7ecef268fd54587afc5d357b481f3bb8))
* **test:** stability should come from matrix.stability variable ([2264e98](https://github.com/99linesofcode/.github/commit/2264e98085db7120648de6d02a68680868037c39))
* **test:** use dedicated .env.testing.github dotenv ([0042bae](https://github.com/99linesofcode/.github/commit/0042bae77784271ccdfe006ec4f08e92edb77d4f))
* **workflow:** don't run on .github itself ([e450b7f](https://github.com/99linesofcode/.github/commit/e450b7f38f69fa6a3353fbbe94f11e741146f1ca))
* **workflow:** run migration before running PHPUnit tests ([bc93511](https://github.com/99linesofcode/.github/commit/bc9351181ba10048081a7d09da246219fd8d2edc))


### Features

* callable github action for testing laravel applications with phpunit ([d834148](https://github.com/99linesofcode/.github/commit/d834148553f77f32f9f0e8263bbe30aedc5d488c))
* **changelog:** create a lightweight tag ([f94c512](https://github.com/99linesofcode/.github/commit/f94c5129403acdadc7ac5a516634268976a5a665))
* **changelog:** create Github release ([885da38](https://github.com/99linesofcode/.github/commit/885da382a7a47890db61e9f33bf0267268435f4d))
* **changelog:** scaffold changelog workflow ([1e715cf](https://github.com/99linesofcode/.github/commit/1e715cf83b4bfcb71e322432b3dbcd7e25ea07cc))
* **changelog:** trigger changelog generation for this repo as well ([b125875](https://github.com/99linesofcode/.github/commit/b12587505f65d2dcf09034b3d24da72d18180eb6))
* **deploy:** pass in decryption key from calling repository ([2bedcad](https://github.com/99linesofcode/.github/commit/2bedcadef314afec80db9ca795af10681f465b12))
* **deploy:** pass in remaining secrets from caller repository ([b9789c3](https://github.com/99linesofcode/.github/commit/b9789c3621f857591f610920ba2ec10623616cde))
* **test:** accept caller input for database name ([6f4af0e](https://github.com/99linesofcode/.github/commit/6f4af0e93d3ba36150aea514a9dd83d314084260))
* **test:** enable test coverage reporting ([131ae9a](https://github.com/99linesofcode/.github/commit/131ae9a9d6bd56ad56d145f1bb8a80a3f0249e3f))
* **workflow:** add soketi service for feature testing ([a6ed8c4](https://github.com/99linesofcode/.github/commit/a6ed8c45fb727b33e0c46b14668e8116d131bc3b))
* **workflow:** automatic deployment using Kamal ([82672dc](https://github.com/99linesofcode/.github/commit/82672dc1e8ca15705bc3ac3b3fe914c717f3384d))



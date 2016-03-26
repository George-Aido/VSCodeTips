## VSCodeTips

## Important

This guide assumes that you have `npm` installed in your system. If this is not true you can find how to install it and more details [here][npm]. 

## Node Version Manager:

##### To install or update `nvm`, you can use the [install script][nvm_install] using cURL:

    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash

<sub>The script clones the nvm repository to `~/.nvm` and adds the source line to your profile (`~/.bash_profile`, `~/.zshrc` or `~/.profile`).</sub>

##### List of all the available versions of `node.js`:

    nvm ls-remote

##### List of all the installed versions of `node.js`:

    nvm ls
        
##### Install version “x.x.x”. Replace "x" with your version:

    nvm install x.x.x
        
##### Switch back to version “y.y.y” (should be installed first). Replace "x" with your version:

    nvm use y.y.y
        
##### Get the path to the executable to where it was installed:

    nvm which x.x.x
    
##### To set a default Node version to be used in any new shell, use the alias 'default':

    nvm alias default node

##### Use node system version:

    nvm use system

More details about `NVM` can be found [here][nvm].


## Important packages.

##### Check outdated npm packages (globally):

    npm outdated -g --depth=0

##### Update all global packages (globally):
        
    npm update -g

##### Show globally installed `npm` packages:
    
    npm list -g --depth=0
    
## ESLint

##### What's a linter?

A linter is a static code analysis tool that points out common mistakes and potential bugs in source code, as well as stylistic errors. 

##### What about `ESLint`?

ESLint is an open source JavaScript linting utility originally created by Nicholas C. Zakas in June 2013. Code [lintinging][eslint_wiki] is a type of static analysis that is frequently use to find problematic patterns or code that doesn't adhere to certain style guidelines. There are code linters for most programming languages, and compilers sometimes incorporate linting into the compilation process.
More about `ESLint` [here][eslint].

##### How do I start with ESLint in VSCode?

- You should first have `eslint` installed in your system. Here is how to do this: 

        npm install -g eslint
    
- After that you should also install the [ESLint extension][vscode_eslint]. Then, in a terminal, navigate to your project's folder and type:
        
        eslint --init
    
A few options should appear for you to choose. You can either answer some questions about your preferences and style or you can choose a predefined one.

Once that is done you should have a `.eslintrc` file inside your project where you can configure the linter.
More about configuring this file can be found [here][eslint_conf].
        
[npm]: https://github.com/npm/npminiteslint
[nvm_install]: https://github.com/creationix/nvm/blob/v0.31.0/install.sh
[nvm]: https://github.com/creationix/nvm.git
[eslint]: https://github.com/eslint/eslint
[eslint_wiki]: http://en.wikipedia.org/wiki/Lint_(software)
[eslint_conf]: http://eslint.org/docs/user-guide/configuring
[vscode_eslint]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint

what is create react app ?
it is already ignited with all the react super power. 
it gives the basic react app which is already production ready.
--------------------------------

package.json is configuration for npm.

why do we need package.json file?
package and  dependencies are one thing.
npm take care of what is the version of that package and it will take care of it in package.json file.
--------------------------------


package-lock.json  locks the version  and keeps the record of exact version of it.
package-lock.json keeps hash to  verify that whatever is there in my machine is the same version to be deployed onto the production
package.json keeps the approximate version of it
--------------------------------


what is bundler ?

bundler  do   minification , caching , cleaning compressing  before it need to be send to production .

create react app use webpack bundler.
--------------------------------

there are two types of dependencies(package) :
a. dev-dependencies (used in development phase)
b. normal-dependencies (used in production phase also) 
--------------------------------

**transitive dependencies**(dependencies having their own dependencies) 
--------------------------------

why to keep package.json and package-lock.json to git ?

maintains the note of what dependencies our project needs.
but not to put node_modules in git as if we have package.json and package-lock.json we can recreate all node_modules.
so, whatever we can recreate will not put in git.
--------------------------------

**which is the best way to use react by cdn scrpit or npm i react ?
npm is best way as cdn is expensive to use and though npm we have react code in our node_modules folder. npm manage version well 
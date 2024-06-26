Q. What is `NPM`?

NPM does not stands for node package manager.
NPM is the package manager for js maintained by npm.
NPM is the default package manager for Node.js.
It allows developers to manage dependencies, install packages, and share reusable code modules (packages) with ease.
----------------------------------------------------------------
Q. What is `Parcel/Webpack`? Why do we need it?

Parcel is a bundler.
Parcel is a powerful bundler package that offers several advantages for web development:
-    Zero Configuration.
- tree shaking removing unwanted code
- Dev Build
- Local Server
- HMR = Hot Module Replacement
- File Watching Algorithm - written in C++
- Caching - Faster Builds
- Image Optimization
- Minification
- Bundling
- Compress
- Consistent Hashing
- Code Splitting
- Differential Bundling - support older browsers
- Diagnostic
- Error Handling
- HTTPs
----------------------------------------------------------------
Q. What is `.parcel-cache`?

Parcel caches everything it builds to disk. If you restart the dev server, Parcel will only rebuild files that have changed since the last time it ran.
Parcel automatically tracks all of the files, configuration, plugins, and dev dependencies that are involved in your build, and granularly invalidates the cache when something changes. For example, if you change a configuration file, all of the source files that rely on that configuration will be rebuilt.

By default, the cache is stored in the .parcel-cache folder inside your project. You should add this folder to your .gitignore (or equivalent) so that it is not committed in your repo.
----------------------------------------------------------------

**Q. what is npx?**
Node Package Execute (npx) is a utility for running Node.js packages directly from the command line.
It allows you to execute any package (either locally installed or fetched remotely) without explicitly installing it globally or locally.
With npx, you can run a package without installing it first.
It fetches the package from the npm registry and executes it.
----------------------------------------------------------------
Q. What is difference between `dependencies` vs `devDependencies?

In your package.json file, the dependencies and devDependencies serve distinct purposes:

dependencies:
These are essential packages required for your production-ready site or app to function correctly.
When your application runs in a production environment (i.e., the version that your audience experiences online), it relies on these dependencies.

devDependencies:
These packages are used during development but are not necessary for production.
They support tasks related to building, testing, and maintaining your codebase.
Examples include:
Build Tools: Webpack, Babel, or Parcel.
----------------------------------------------------------------
Q. What is Tree Shaking?

Tree shaking is a term commonly used within a JavaScript context to describe the removal of dead
code.

It relies on the import and export statements to detect if code modules are exported and imported
for use between JavaScript files.

In modern JavaScript applications, we use module bundlers (e.g., webpack or Rollup z) to
automatically remove dead code when bundling multiple JavaScript files into single files. This is
important for preparing code that is production ready, for example with clean structures and minimal
file size.
----------------------------------------------------------------

Q. What is Hot Module Replacement?

Hot Module Replacement (HMR) is a powerful feature in modern web development that significantly improves the developer experience during code changes
HMR allows you to update parts of your application without a full page reload.
When you make changes to your code (such as modifying a component or CSS), HMR automatically applies those changes in the running application.
When you save changes, the runtime detects which modules have been modified.
It then replaces only those modules in the running application
benefits:
Instant Feedback: You see changes immediately without refreshing the entire page.
Preserved State: HMR keeps your application state intact during updates.
Faster Iteration: Developers can iterate quickly, improving productivity.
----------------------------------------------------------------

Q.  List down your favourite 5 superpowers of Parcel and describe any 3 of them in yourown words.

  HMR(hot module replacement)
  minification -> reduces the number of line of code .
                  Minification reduces the file size of your output bundles by removing whitespace, renaming variables to shorter names, and many other 
  optimizations.
                  
  tree shaking -> removal of unwanted line of code or unused code.
  diff: tree shaking focuses on removing unused modules or functions from the codebase, while minification focuses on reducing the size of the code by removing 
  unnecessary characters and optimizing its structure.
  image optimisation.
  caching -> it caches everything it build and saves the time  at the time of rebuild by building the new file .
----------------------------------------------------------------

Q. What is the difference between `package.json` and `package-lock.json?

package.json:
Contains metadata about the project and its dependencies.
Project information: Name, version, description, author, license, etc.
Dependency management: Lists packages required for the project to run (under the "dependencies" section).

package-lock.json:
Role:
Automatically generated file.
Provides a detailed, deterministic record of the dependency tree.
Contents:
Exact versions of every installed package.
Resolved details (URLs, integrity hashes) for each package.

Usage:

package.json:
Developers manually create and maintain it.
Contains high-level project configuration.
Used for installing dependencies (npm install).

package-lock.json:
Automatically generated by npm.
Records exact versions and resolved details.
Ensures consistent builds and faster installations.
----------------------------------------------------------------

Q. Why should I not modify `package-lock.json`?

The package-lock.json file is automatically generated and maintained by npm or Yarn to lock down the versions of dependencies installed in your project.

Here are reasons :
Dependency Consistency: The purpose of package-lock.json is to ensure that all developers working on a project have consistent dependency versions.
Manually modifying this file can lead to inconsistencies between different environments and cause issues when collaborating with other developers.

Security and Stability: Modifying package-lock.json can introduce security vulnerabilities or stability issues by installing incompatible or outdated dependency versions. 
The lock file ensures that only verified and compatible versions of dependencies are installed.

Version Control: package-lock.json is intended to be checked into version control to provide a consistent dependency environment for the project. 
Manually modifying the lock file can lead to conflicts in version control and make it difficult to maintain a reliable dependency configuration.
----------------------------------------------------------------

Q. What is `node_modules` ? Is it a good idea to push that on git?

node_modules is a directory created by npm (Node Package Manager) to store dependencies for your Node.js project.
node_modules contains all the code that we fetch from npm .
node_modules is like database it contains the actual data .
The node_modules folder contains all the external packages (libraries, modules, utilities) that your project depends on.
When you install packages using npm install, they are downloaded and stored in this directory.

Why Is It Important?:
Dependency Management: node_modules ensures that your project has access to the required packages.

Should You Push node_modules to Git?:
Generally No.
----------------------------------------------------------------

Q. what is dist folder?

The dist folder, short for “distribution,” plays a significant role in web development projects.

Purpose:
The dist directory contains the compiled and optimized version of your project.
is a production-ready compiled version of your code.

The dist folder is typically generated by build tools like Webpack, Parcel, or Gulp.
During the build process, these tools bundle, minify, and optimize your code, placing the result in the dist directory.
----------------------------------------------------------------

Q. what is browserslist?

Browserslist is a configuration tool that allows developers to specify a target list of browsers for their projects. 
It is widely used in various front-end tools and libraries to optimize code and styles for different browser environments.

----------------------------------------------------------------
Q.  ^ - caret and ~ - tilde

The caret symbol (^) is used to specify a range of compatible versions with the following rules:
If the specified version is X.Y.Z, npm will allow installing any version X.(Y+1).(Z+1) up to, but not including, the next major version ((X+1).0.0).
For example, "^1.2.3" allows installing versions 1.2.3, 1.3.0, 1.4.0, etc., but not 2.0.0.

The tilde symbol (~) is used to specify a range of compatible versions with the following rules:
If the specified version is X.Y.Z, npm will allow installing any version X.Y.(Z+1) up to, but not including, the next minor version (X.(Y+1).0).
For example, "~1.2.3" allows installing versions 1.2.3, 1.2.4, 1.2.5, etc., but not 1.3.0.
---------- 

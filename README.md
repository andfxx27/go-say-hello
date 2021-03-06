# go-say-hello
A simple go module demonstration.

---

## Tag
Create tag for current project
1. `git tag version_name`.
2. `git push origin main version_name`.

---

## Upgrade Module Version
To upgrade your module version, please follow below steps for:

### Module Developer 
If you are developing a go module and want to update its version, you can create new git release tag with the updated version.

### Module User (Upgrade Dependency)
If you are depending on a certain go module/ dependency and want to upgrade your dependency's version, you can do:
1. Upgrade the stated module version in `go.mod` file. In the example image below, change the underlined part to the release tag version you want (also make sure the module provide release tag for the corresponding version).
![image](https://user-images.githubusercontent.com/52846032/123961604-bc4a0e80-d9da-11eb-9a8c-c0916bc94775.png)

2. Run `go get` to get the latest go module version release.

---

## Major Upgrade for Module Version
If there is an upgrade for a module, which causes a break in code (not backward compatible), there are several ways to handle this like so:

### Module Developer
1. Code all the changes for the major module upgrade.
2. **Change** the module name for the next major version by adding 'v*' (with * being a version number), for example: `github.com/andfxx27/go-say-hello` to `github.com/andfxx27/go-say-hello/v2`, and after that you can commit and push the changes (you can use the current branch or create an entirely new branch for the major upgrade).
3. Create new release tag for the corresponding major upgrade version.

### Module User (Upgrade Dependency)
1. **Remove** the required module from `go.mod` file which undergo a major upgrade.
2. Get the new module upgrade by using command `go get new_module_name_with_major_upgrade`, in the case of go-say-hello module, you can use the command `go get github.com/andfxx27/go-say-hello/v2`.
3. Since a major upgrade **usually** breaks the code, make further adjustment inside the application following the updated module.

---

## How to
If you want to add this module as dependency for your project, you can follow the command: `go get github.com/andfxx27/go-say-hello`.

---

## Inspiration and special thanks
Special thanks to [Programmer Zaman Now](https://www.youtube.com/c/ProgrammerZamanNow/videos) YouTube Channel for the go-module learning material.

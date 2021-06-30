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
## How to
If you want to add this module as dependency for your project, you can follow the command: `go get github.com/andfxx27/go-say-hello`.

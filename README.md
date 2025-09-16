# libpanda-default-apps
Example structure of libpanda apps

# how to create a new libpanda app

In order to create a new app structure, you should already have created the following:
1. A github repository with no spaces, capital letters, or special characters, which is your ros package
2. A launchfile that will run your system, in the `${REPONAME}/launch/` folder

With these already created, along with any other code you have

```
cd catkin_ws/src/yourpackage
./relative/path/to/libpanda-default-apps/createNewPandaApp.sh
```

Follow the instructions, giving your github username, and the package name. Once this is done, you should have

```
yourpackage
|
-- launch/
  |
  -- yourpackage.launch
  -- yourpckagedocker.launch
|
-- src/
  |
  -- (your source files
-- yourpackage/
  |
  -- {install,installController,installRosPackages,start,stop,uninstall}.sh
  -- description.txt
  -- service
```

On the raspberrypi installed in the car, you now install the package

```
sudo libpanda-app-manager -g
```

Enter the git user and repository details, and it should install everything!

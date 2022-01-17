# Small Targets Experiment

This repository contains a [FPSci](https://github.com/NVLabs/FPSci) user study experiment to test the performance of the user on small targets. It was designed to compare a 24.5" 1080p 360 Hz screen to a 27" 1440p 360 Hz screen, the results of which can be found in [this blog post](https://developer.nvidia.com/blog/improving-aiming-time-on-small-fps-targets-with-higher-resolutions-and-larger-screen-sizes/).

## How to run

1. Double click `setup.bat`, which will download the required version of FPSci, and copy the experiment configuration files into the right location.
2. Double click `RunFPSci.bat` or double click on `FirstPersonScience.exe` inside the `FPSci` directory (created by the download and extract in `setup.bat`).
3. Create a new user by entering a name and clicking the `Create User` button. If you're different screens, it's useful to put the screen you're using in your user name (`name_24` for example).
4. (optional) Use the in-game menu to adjust mouse sensitivity to your preferred value.
5. After the experiment, there will be a results file for each user name in the results directory that you can analyze.
6. (optional) If something goes wrong and you need to start over, you can delete the `FPSci` directory, and return to step 1 above.
7. (optional) If you're comparing 2 or more screens, you'll want to repeat steps 2-5 creating another new user for each screen you use. It may be helpful to note the mouse sensitivity you used the first time to keep that the same on different screens.

## More about mouse sensitivity

If you know your mouse sensitivity in cm/360, then you can type the value you want in using the deg/mm box. If your cm/360 is `C` then `deg/mm = 36/C` so you can divide 36 by your cm/360 to get the value to type in. If you do this, then if your mouse driver setting has a DPI other than 800, you'll need to manually change the DPI setting in `FPSci/userconfig.Any` after creating your new user, and quitting FPSci. Once you change the value in the file, you can run FPSci again and it will use the correct DPI setting. This extra work is because FPSci currently has no way to automatically detect mouse DPI settings.

## Need help with analysis?

The results file is a [sqlite](https://www.sqlite.org/index.html) database file. You can find instructions online to export tables from sqlite to csv or other formats online. An overview of the schema FPSci uses can be found in the [FPSci documentation](https://github.com/NVlabs/FPSci/blob/v21.10.02/docs/resultsFiles.md).

If you need help with analysis, you can send a direct message to [Josef Spjut](https://twitter.com/josefspjut) on twitter.

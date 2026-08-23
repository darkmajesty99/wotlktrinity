#### Installation

Available as:
- Direct merge: https://github.com/Rochet2/TrinityCore/tree/transmogvendor_3.3.5
- Diff: https://github.com/Rochet2/TrinityCore/compare/TrinityCore:3.3.5...transmogvendor_3.3.5.diff
- Diff in github view: https://github.com/Rochet2/TrinityCore/compare/TrinityCore:3.3.5...transmogvendor_3.3.5

Using direct merge:
- open git bash to source location
- do `git remote add rochet2 https://github.com/Rochet2/TrinityCore.git`
- do `git pull rochet2 transmogvendor_3.3.5`
- optionally tweak the config settings in `src/server/game/Entities/Item/TransmogDisplayVendor.cpp`
- use cmake and compile

Using diff *(recommended)*:
- DO NOT COPY THE DIFF DIRECTLY! It causes apply to fail.
- download the diff by __right clicking__ the link and select __Save link as__
- place the downloaded `transmogvendor_3.3.5.diff` to the source root folder
- open git bash to source location
- do `git apply transmogvendor_3.3.5.diff`
 - if using the regular transmogrification, simply use --reject with either and overwrite the parts of the other. Order doesnt matter, as long as duplicate code doesnt exist.
- optionally tweak the config settings in `src/server/game/Entities/Item/TransmogDisplayVendor.cpp`
- use cmake and compile

After compiling:
- TrinityCore auto updater should run needed SQLs automatically.
- If you do not use the auto updater then run files named `*_transmogvendor.sql` from `\sql\custom` to your databases.
- Optionally you can also insert a transmogrifier NPC to your database by running `\src\server\scripts\Custom\TransmogDisplayVendor\sql\world_NPC.sql` to your world database.

#### Usage
Equip an item that is suitable for transmogrification.
Talk to Transmogrifier and select the item slot. Then select the quality and then the item you want to transmogrify to.

#### Bugs and Contact
Report issues and similar to http://rochet2.github.io/

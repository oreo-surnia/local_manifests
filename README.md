# local_manifests for this repos
There it is some changes to use a stable source to build LOS15 or LOS-Based ROMs on moto msm8916 devices (mostly surnia, but there's osprey, harpia and more). If you got some change or suggestion or fix for your device, feel free to pull request idk.

## How can i add this to my common repo sync?
by just ctrl+c and ctrl+v this:
```
curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/oreo-surnia/local_manifests/master/local_manifest.xml
```

## How many changes do i have to do?
**Required:**

bionic: repopick [185640](https://review.lineageos.org/#/c/185640/) [190614](https://review.lineageos.org/#/c/190614/) 

frameworks/av: repopick [187558](https://review.lineageos.org/#/c/187558/) [187559](https://review.lineageos.org/#/c/187559/) [187560](https://review.lineageos.org/#/c/187560/) [187561](https://review.lineageos.org/#/c/187561/) [188388](https://review.lineageos.org/#/c/188388/) (note: this one it's a workaround by now).

hardware/qcom/audio-caf/msm8916: repopick [189434](https://review.lineageos.org/#/c/189434/) [189435](https://review.lineageos.org/#/c/189435/) [189436](https://review.lineageos.org/#/c/189436/) [189437](https://review.lineageos.org/#/c/189437/)

system/qcom: repopick [187637](https://review.lineageos.org/#/c/187637)

**Optional:**

build/make: repopick [186687](https://review.lineageos.org/#/c/186687/) (this needs an updated TWRP with #define TW_NO_LEGACY_PROPS 1 added.)

system/core: repopick [187146](https://review.lineageos.org/#/c/187146)


## The test branch
There will be a test branch to mess up and if every new change works fine, will be merged on main branch

## Credits
This is thanks to alberto97, the main dev of moto msm8916 for Lineage, he made almost everything, also thanks to droidfreak32 who was working hard to make camera and stuff work, and well, a small thanks to me, eldainosor who fixed the init for surnia. be sure to credit to people who made this possible idk

also, don't be a [lazybone](https://gist.github.com/eldainosor/84bb9f911385b573712d9e932fa549d3) and have fun building oreo :)

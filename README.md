# chromium-vaapi-ubuntu
Set of modifications needed to compile Chromium with vaaapi support on Ubuntu, using the debian package sources

- **chromium-vaapi.patch** in **debian/patches**
- **series** in debian/patches with **chromium-vaapi.patch** on it, needed to apply the patch when the package is built
- **use_vaapi=true** in **debian/rules**
- **libva-dev** as a build dependency in **debian/control**

## Latest Chromium version tested working with this patch: 
- [x] 75.0.3770.90 

### Notes on AMD GPU's: 
There is a bug with AMD GPU's https://bugs.freedesktop.org/show_bug.cgi?id=108937 not showing the correct color information to the device driver, the workaround needed is to edit your environment variables before running chromium with ```allow_rgb10_configs=false```
- [x]

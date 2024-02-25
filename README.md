# Reverse-engineers
1. Tools for Reverse Engineers:
  + JADX: https://github.com/skylot/jadx
  + APKTool: https://apktool.org/
  + Proxyman: https://proxyman.io/
  + Adb
2. How to decompile and re-compile apk:
  + Install Apktool on Mac: ```brew install apktool```
  + Decompile apk: ```apktool d foo.apk``` (https://apktool.org/docs/the-basics/decoding)
  + Re-compile apk: ```apktool b foo_folder -o new_foo.apk``` (https://apktool.org/docs/the-basics/building)
  + Generate keystore: ```keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000```
  + ```zipalign -p 4 new_foo.apk new_foo2.apk```
  + ```apksigner sign --ks-key-alias alias_name --ks my-release-key.keystore new_foo2.apk``` (https://stackoverflow.com/questions/10930331/how-to-sign-an-already-compiled-apk)
3. Setup Android physical device to catch network requests on Proxyman
  

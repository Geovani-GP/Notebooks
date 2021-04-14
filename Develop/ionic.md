# IONIC

## Nuevo Proyecto

## Iniciar servidor de ionic
ionic serve

## Con Angular añadir Material
ng add @angular/material

## Iniciar depuración en el telefono conectado
ionic cordova run android --prod

##Iniciar depuración en tiempo real telefono y computadora
ionic cordova run android --prod -l

## Iniciar el depurador de Chrome
chrome://inspect/#devices

# Firmar APK

## Release al proyecto ionic
ionic cordova build android --prod --release

## Crear firma privada:
keytool -genkey -v -keystore { my-key.keystore } -alias { keystore } -keyalg RSA -keysize 2048 -validity 10000
                               nombre de la key          alias name

## Firmar apk
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore C:\Users\dti-c\OneDrive\Documentos\KeyStore\GreenPet\greenpet.keystore app-release-unsigned.apk keystore

## Optimizar apk firmada:
zipalign -v 4 app-release-unsigned.apk app-signed.apk

---

alias: keystore

C:\Users\dti-c\OneDrive\Documentos\KeyStore\ShopSi\shopsi.keystore
C:\Users\dti-c\OneDrive\Documentos\KeyStore\Mosandi\mosandi.keystore
C:\Users\dti-c\OneDrive\Documentos\KeyStore\GreenPet\greenpet.keystore

/_ ShopSi APK _/
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore C:\Users\dti-c\OneDrive\Documentos\KeyStore\ShopSi\shopsi.keystore app-release-unsigned.apk shopsi

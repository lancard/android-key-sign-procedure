# android-key-sign-procedure
안드로이드 사인 절차 (CLI)

# keystore 생성 (100년 짜리)
- keytool -genkey -v -keystore worstrocker.keystore -alias worstrocker -keyalg RSA -keysize 4096 -validity 36500
- 암호 입력 후 이름 및 KR 한국 코드 입력 후 yes

# keystore로 서명
- cordova build --release -- --keystore=worstrocker.keystore --storePassword=(암호) --alias=worstrocker --password=(암호) --packageType=bundle

# 참고사항
- Release build는 잘되는데, Debug 빌드가 zip64 어쩌구 하면서 빌드 안되면 사이즈가 너무 커서다.

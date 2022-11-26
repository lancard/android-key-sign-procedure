# android-key-sign-procedure
안드로이드 사인 절차 (CLI)

# keystore 생성 (100년 짜리)
keytool -genkey -v -keystore worstrocker.keystore -alias worstrocker -keyalg RSA -keysize 4096 -validity 36500

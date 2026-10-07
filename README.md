# MobileStreamer
Streaming Android (RTMP/RTMPS) berbasis RootEncoder, Kotlin, landscape.

## Build APK
**Android Studio:** File > Open folder ini > tunggu Sync > Build > Build APK(s).
APK: app/build/outputs/apk/debug/app-debug.apk
**Tanpa Android Studio:** push folder ini ke repo GitHub; tab Actions > "Build APK" > unduh artifact.

## Catatan teknis
- 50i: encoder hardware Android (MediaCodec) hanya progresif. "50i" dikirim sebagai 25 frame/detik
  (kadens setara 50 field/detik). Untuk gerak halus asli gunakan 50p.
- Resolusi & FPS yang tampil mengikuti kemampuan kamera perangkat; kombinasi tak didukung akan ditolak dengan pesan.
- Analisis jaringan: RTT/jitter/loss probe TCP ke server + bitrate kirim aktual dari encoder.

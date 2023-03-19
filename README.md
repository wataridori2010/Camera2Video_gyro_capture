# Android app to capture original gyro and video data. 

- this app is based on "old" Android Camera2Video Sample app

## Environments
- Android stuido 3.1
- android-ndk-r17c
- CAUTION: you need to set some permissions to allow capture video, voice data and store in android app. 																																												


## Output files
- 'yyyymmdd_hhmmss.mp4'       : non-stabilized video data
- 'yyyymmdd_hhmmss_gyro.csv'  : timeStamp, gyrox, gyroy, gyroz
- 'yyyymmdd_hhmmss_frame.csv' : timeStamp, frame index, exposure, frame duration


---
- misc
 - mi9の場合だと、データ保存先は　PC\MI 9\内部共有ストレージ\Pictures\Recorder
 - camera2videoにonSensorChangedを追記しただけではジャイロを取得できない。sensorMangerを書かないといけない 
 - このままではNDKが使われてないと思ってたが、bundleのNDKではエラーが出たので外部のndkを指定した
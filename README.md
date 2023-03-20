# Android app to capture original gyro and video data. 

- this app is based on "old" Android Camera2Video Sample app

## Environments
- Android stuido 3.1
- android-ndk-r17c


## Output files
- 'yyyymmdd_hhmmss.mp4'       : non-stabilized video data
- 'yyyymmdd_hhmmss_gyro.csv'  : timeStamp, gyrox, gyroy, gyroz
- 'yyyymmdd_hhmmss_frame.csv' : timeStamp, frame index, exposure


## misc
 - アプリ側でストレージも許可する必要アリ
 - mi9の場合だと、データ保存先は　PC\MI 9\内部共有ストレージ\Pictures\Recorder
 - camera2videoにonSensorChangedを追記しただけではジャイロを取得できない。sensorMangerを書かないといけない 
 - このままではNDKが使われてないと思ってたが、bundleのNDKではエラーが出たので外部のndkを指定した
 - buildして...INVALID-APKというエラーが出た場合、clean projectして再ビルドする
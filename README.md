# Components

## cupertino 

### import 
```dart
import 'package:laudyou_app/screens/components/cupertino.dart';
```

### paramter(...)

| Param         | Type                                                | Contents                                            |
| ------------- | --------------------------------------------------- | --------------------------------------------------- |
| **`list`** | List<String> | 콤보박스 노출 리스트 |
| **`width`** | double | 넓이 |
| **`height`** | double | 높이 |
| **`onSelectedItemChanged`** | ValueChanged(int)| 선택하 인덱스 콜백 |
  
### example
```dart
Cupertino(
  width: 200,
  height: 48,
  list: timeList
      .map((e) =>
          "하루 ${UtilCommon.hour(e["time"])} 이상")
      .toList(),
  onSelectedItemChanged: (i) => {
    _selectTime =
        timeList[i]["time_id"],
    debugPrint('인덱스 $i'),
    debugPrint('타임 키 $_selectTime')
  }
)
```

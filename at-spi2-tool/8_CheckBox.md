# CheckBox

TizenFX에 있는 Tizen.NUI.StyleGuide 샘플을 사용하여 확인했습니다.

`CheckBox` class를 확인하기 위해 

[CheckBoxExample.cs](https://github.com/Samsung/TizenFX/blob/master/test/Tizen.NUI.StyleGuide/Examples/CheckBoxExample.cs) 샘플을 통해 at-spi2-tool을 동작시켜 보았습니다.

![CheckBox](./images/8.CheckBox.png)

왼쪽은 mobile emulator에서 샘플을 런칭한 화면이고, 오른쪽은 at-spi2-tool로 확인한 tree node입니다.

<br>

```
[[node],[node role name],[attributes list],[x,y,width,height],[node name],[states list][relations]

[[:1.268:root],[application],[toolkit=dali],[(null)],[_,_,_,_],[org.tizen.example.Tizen.NUI.Samples],[(null)],[]]
  [[:1.268:0x808357bc],[window],[toolkit=dali],[(class=Layer)],[0,0,720,1280],[RootLayer],[(ACTIVE)(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
    [[:1.268:0x80a003cc],[redundant object],[toolkit=dali],[(class=CameraActor)],[360,640,0,0],[DefaultCamera],[(SHOWING)(VISIBLE)],[]]
    [[:1.268:0x80d43cf8],[unknown],[toolkit=dali],[(class=Control)],[0,0,720,1280],[],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
      [[:1.268:0x80a8ef38],[check box],[toolkit=dali],[(class=CheckBox)],[170,590,100,100],[],[(ENABLED)(FOCUSABLE)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTED)(HIGHLIGHTABLE)],[]]
        [[:1.268:0x80f25538],[image],[toolkit=dali],[(class=ImageView)(highlight=)],[170,590,100,100],[],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
      [[:1.268:0x80a8aef8],[check box],[toolkit=dali],[(class=CheckBox)],[310,590,100,100],[],[(CHECKED)(FOCUSABLE)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTABLE)],[]]
      [[:1.268:0x809fc5c8],[check box],[toolkit=dali],[(class=CheckBox)],[450,590,100,100],[],[(CHECKED)(ENABLED)(FOCUSABLE)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTABLE)],[]]

```

<br>

### `AccessibilityName`이 필요한 곳?
 : 비쥬얼 요소로 텍스트가 있는 Component

- N/A

<br>

### `AccessibilityHidden` 적용을 위해 고려할 사항

- N/A


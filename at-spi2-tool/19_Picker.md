# Picker

- DatePicker와 TimePicker 모두 결국은 Picker 클래스로 이루어진 것이기 때문에
 Picker를 통해 우선 at-spi2 tree node를 줄여보고자 추가한 페이지입니다.

[PickerSample.cs](https://github.com/Samsung/TizenFX/blob/master/test/Tizen.NUI.Samples/Tizen.NUI.Samples/Samples/PickerSample.cs) 샘플을 통해 at-spi2-tool을 동작시켜 보았습니다.

<br>

```
// 변경 전

[[node],[node role name],[attributes list],[x,y,width,height],[node name],[states list][relations]

[[:1.17:root],[application],[toolkit=dali],[(null)],[_,_,_,_],[org.tizen.example.Tizen.NUI.Samples],[(null)],[]]
  [[:1.17:0xb7873554],[window],[toolkit=dali],[(class=Layer)],[0,0,720,1280],[RootLayer],[(ACTIVE)(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
    [[:1.17:0xb78d867c],[redundant object],[toolkit=dali],[(class=CameraActor)],[360,640,0,0],[DefaultCamera],[(SHOWING)(VISIBLE)],[]]
    [[:1.17:0xb7f59918],[list],[toolkit=dali],[(class=Picker)],[280,471,160,339],[],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
      [[:1.17:0xb7a67ca0],[unknown],[toolkit=dali],[(class=PickerScroller)],[280,471,160,339],[pickerScroller],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
        [[:1.17:0xb7ad0c20],[unknown],[toolkit=dali],[(class=Control)],[280,-969,160,3600],[ContentContainer],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
          [[:1.17:0xb7ab6ca0],[label],[toolkit=dali],[(class=TextLabel)],[280,-969,160,72],[One],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7ab3758],[label],[toolkit=dali],[(class=TextLabel)],[280,-897,160,72],[Two],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7aad160],[label],[toolkit=dali],[(class=TextLabel)],[280,-825,160,72],[Three],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a7fb90],[label],[toolkit=dali],[(class=TextLabel)],[280,-753,160,72],[Four],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a3dc38],[label],[toolkit=dali],[(class=TextLabel)],[280,-681,160,72],[Five],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a39930],[label],[toolkit=dali],[(class=TextLabel)],[280,-609,160,72],[Six],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a336e0],[label],[toolkit=dali],[(class=TextLabel)],[280,-537,160,72],[Seven],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a6c100],[label],[toolkit=dali],[(class=TextLabel)],[280,-465,160,72],[Eight],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a796a8],[label],[toolkit=dali],[(class=TextLabel)],[280,-393,160,72],[Nine],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a05488],[label],[toolkit=dali],[(class=TextLabel)],[280,-321,160,72],[Ten],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a6f1a0],[label],[toolkit=dali],[(class=TextLabel)],[280,-249,160,72],[One],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a64980],[label],[toolkit=dali],[(class=TextLabel)],[280,-177,160,72],[Two],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a491f0],[label],[toolkit=dali],[(class=TextLabel)],[280,-105,160,72],[Three],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a09930],[label],[toolkit=dali],[(class=TextLabel)],[280,-33,160,72],[Four],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a01340],[label],[toolkit=dali],[(class=TextLabel)],[280,39,160,72],[Five],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a2b878],[label],[toolkit=dali],[(class=TextLabel)],[280,111,160,72],[Six],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a13c30],[label],[toolkit=dali],[(class=TextLabel)],[280,183,160,72],[Seven],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a18260],[label],[toolkit=dali],[(class=TextLabel)],[280,255,160,72],[Eight],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb78d2bf8],[label],[toolkit=dali],[(class=TextLabel)],[280,327,160,72],[Nine],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb78d5ae0],[label],[toolkit=dali],[(class=TextLabel)],[280,399,160,72],[Ten],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb79fdca8],[label],[toolkit=dali],[(class=TextLabel)],[280,471,160,72],[One],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb79f6f80],[label],[toolkit=dali],[(class=TextLabel)],[280,543,160,72],[Two],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb79e5920],[label],[toolkit=dali],[(class=TextLabel)],[280,615,160,72],[Three],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTED)(HIGHLIGHTABLE)],[]]
            [[:1.17:0xb7bf4d10],[image],[toolkit=dali],[(class=ImageView)(highlight=)],[280,615,160,72],[],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
          [[:1.17:0xb7ba0e50],[label],[toolkit=dali],[(class=TextLabel)],[280,687,160,72],[Four],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7af8310],[label],[toolkit=dali],[(class=TextLabel)],[280,759,160,72],[Five],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7aeb008],[label],[toolkit=dali],[(class=TextLabel)],[280,831,160,72],[Six],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a97790],[label],[toolkit=dali],[(class=TextLabel)],[280,903,160,72],[Seven],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a9bcb0],[label],[toolkit=dali],[(class=TextLabel)],[280,975,160,72],[Eight],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7ac5eb8],[label],[toolkit=dali],[(class=TextLabel)],[280,1047,160,72],[Nine],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7ad9710],[label],[toolkit=dali],[(class=TextLabel)],[280,1119,160,72],[Ten],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7add848],[label],[toolkit=dali],[(class=TextLabel)],[280,1191,160,72],[One],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7ae41d8],[label],[toolkit=dali],[(class=TextLabel)],[280,1263,160,72],[Two],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7ad0da8],[label],[toolkit=dali],[(class=TextLabel)],[280,1335,160,72],[Three],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7a3a518],[label],[toolkit=dali],[(class=TextLabel)],[280,1407,160,72],[Four],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb784ea08],[label],[toolkit=dali],[(class=TextLabel)],[280,1479,160,72],[Five],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da1458],[label],[toolkit=dali],[(class=TextLabel)],[280,1551,160,72],[Six],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7bb6808],[label],[toolkit=dali],[(class=TextLabel)],[280,1623,160,72],[Seven],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7756820],[label],[toolkit=dali],[(class=TextLabel)],[280,1695,160,72],[Eight],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da2148],[label],[toolkit=dali],[(class=TextLabel)],[280,1767,160,72],[Nine],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da2330],[label],[toolkit=dali],[(class=TextLabel)],[280,1839,160,72],[Ten],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da19a8],[label],[toolkit=dali],[(class=TextLabel)],[280,1911,160,72],[One],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da1b90],[label],[toolkit=dali],[(class=TextLabel)],[280,1983,160,72],[Two],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7f58da8],[label],[toolkit=dali],[(class=TextLabel)],[280,2055,160,72],[Three],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7f58f90],[label],[toolkit=dali],[(class=TextLabel)],[280,2127,160,72],[Four],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7d9faa0],[label],[toolkit=dali],[(class=TextLabel)],[280,2199,160,72],[Five],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7d9fc88],[label],[toolkit=dali],[(class=TextLabel)],[280,2271,160,72],[Six],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7d9fe70],[label],[toolkit=dali],[(class=TextLabel)],[280,2343,160,72],[Seven],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da0058],[label],[toolkit=dali],[(class=TextLabel)],[280,2415,160,72],[Eight],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da0240],[label],[toolkit=dali],[(class=TextLabel)],[280,2487,160,72],[Nine],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
          [[:1.17:0xb7da0428],[label],[toolkit=dali],[(class=TextLabel)],[280,2559,160,72],[Ten],[(ENABLED)(SENSITIVE)(VISIBLE)(HIGHLIGHTABLE)],[]]
        [[:1.17:0xb78dfdd0],[unknown],[toolkit=dali],[(class=Scrollbar)],[280,471,160,339],[ScrollBar],[(ENABLED)(SENSITIVE)],[]]
          [[:1.17:0xb7aca270],[unknown],[toolkit=dali],[(class=Control)],[424,475,12,331],[],[(ENABLED)(SENSITIVE)(VISIBLE)],[]]
          [[:1.17:0xb7ac19e0],[image],[toolkit=dali],[(class=ImageView)],[424,607,12,31],[],[(ENABLED)(SENSITIVE)(VISIBLE)],[]]
      [[:1.17:0xb784ebf8],[unknown],[toolkit=dali],[(class=Control)],[280,603,160,2],[],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]
      [[:1.17:0xb7b0a010],[unknown],[toolkit=dali],[(class=Control)],[280,675,160,2],[],[(ENABLED)(SENSITIVE)(SHOWING)(VISIBLE)],[]]

```


<br>

```
// 변경 후


```
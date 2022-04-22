# Switch Example

NUI Components의 **키 동작 확인**을 위해 TizenFX에 있는 Tizen.NUI.StyleGuide의 샘플을 확인했습니다.

실행 환경 : Ubuntu 20.04 Terminal

```
seoyeon@seoyeon-linux:~/mywork/develmaster/TizenFX/test/Tizen.NUI.StyleGuide (DevelNUI)$ dotnet run
```

<br>
<br>

[SwitchExample.cs](https://github.com/Samsung/TizenFX/blob/master/test/Tizen.NUI.StyleGuide/Examples/SwitchExample.cs) 샘플을 실행시켰을 때, crash가 발생하여 앱이 실행되지 않습니다.

로그는 아래와 같습니다.

<br>

```C#
OnSelectionChanged() System.Collections.Generic.List`1[System.Object]
selItem.Name=SwitchExample, selItem.FullName=Tizen.NUI.StyleGuide.SwitchExample
INFO: SwitchExample: SwitchExample.cs: .ctor(42) > SwitchExample is contructed
Unhandled exception. System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation.
 ---> System.EntryPointNotFoundException: Unable to find an entry point named 'feedback_initialize' in shared library 'libfeedback.so.0'.
   at Interop.Feedback.Initialize()
   at Tizen.System.Feedback..ctor() in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.System.Feedback/Feedback/Feedback.cs:line 143
   at Tizen.NUI.Components.Control.set_InternalFeedback(Boolean value) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI.Components/Controls/Control.cs:line 143
   at Tizen.NUI.Components.Control.<>c.<.cctor>b__5_0(BindableObject bindable, Object oldValue, Object newValue) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI.Components/Controls/Control.cs:line 44
   at Tizen.NUI.Binding.BindableObject.InternalSetValue(BindableProperty property, Object value) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/public/XamlBinding/BindableObject.cs:line 303
   at Tizen.NUI.Binding.BindableObject.SetValue(BindableProperty property, Object value) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/public/XamlBinding/BindableObject.cs:line 271
   at Tizen.NUI.Components.Control.set_Feedback(Boolean value) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI.Components/Controls/Control.cs:line 127
   at Tizen.NUI.StyleGuide.SwitchExample.CreateSwitchView() in /home/seoyeon/mywork/develmaster/TizenFX/test/Tizen.NUI.StyleGuide/Examples/SwitchExample.cs:line 114
   at Tizen.NUI.StyleGuide.SwitchExample..ctor() in /home/seoyeon/mywork/develmaster/TizenFX/test/Tizen.NUI.StyleGuide/Examples/SwitchExample.cs:line 70
   --- End of inner exception stack trace ---
   at System.RuntimeTypeHandle.CreateInstance(RuntimeType type, Boolean publicOnly, Boolean wrapExceptions, Boolean& canBeCached, RuntimeMethodHandleInternal& ctor, Boolean& hasNoDefaultCtor)
   at System.RuntimeType.CreateInstanceDefaultCtorSlow(Boolean publicOnly, Boolean wrapExceptions, Boolean fillCache)
   at System.RuntimeType.CreateInstanceDefaultCtor(Boolean publicOnly, Boolean skipCheckThis, Boolean fillCache, Boolean wrapExceptions)
   at System.Activator.CreateInstance(Type type, Boolean nonPublic, Boolean wrapExceptions)
   at System.RuntimeType.CreateInstanceImpl(BindingFlags bindingAttr, Binder binder, Object[] args, CultureInfo culture)
   at System.Activator.CreateInstance(Type type, BindingFlags bindingAttr, Binder binder, Object[] args, CultureInfo culture, Object[] activationAttributes)
   at System.Reflection.Assembly.CreateInstance(String typeName, Boolean ignoreCase, BindingFlags bindingAttr, Binder binder, Object[] args, CultureInfo culture, Object[] activationAttributes)
   at System.Reflection.Assembly.CreateInstance(String typeName)
   at Tizen.NUI.StyleGuide.Program.RunSample(String name) in /home/seoyeon/mywork/develmaster/TizenFX/test/Tizen.NUI.StyleGuide/Tizen.NUI.StyleGuide.cs:line 342
   at Tizen.NUI.StyleGuide.Program.OnSelectionChanged(Object sender, SelectionChangedEventArgs ev) in /home/seoyeon/mywork/develmaster/TizenFX/test/Tizen.NUI.StyleGuide/Tizen.NUI.StyleGuide.cs:line 208
   at Tizen.NUI.Components.CollectionView.SelectionPropertyChanged(CollectionView colView, SelectionChangedEventArgs args) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI.Components/Controls/RecyclerView/CollectionView.cs:line 1178
   at Tizen.NUI.Components.CollectionView.<>c.<.cctor>b__151_0(BindableObject bindable, Object oldValue, Object newValue) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI.Components/Controls/RecyclerView/CollectionView.cs:line 54
   at Tizen.NUI.Binding.BindableObject.InternalSetValue(BindableProperty property, Object value) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/public/XamlBinding/BindableObject.cs:line 303
   at Tizen.NUI.Binding.BindableObject.SetValue(BindableProperty property, Object value) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/public/XamlBinding/BindableObject.cs:line 271
   at Tizen.NUI.Components.CollectionView.set_SelectedItem(Object value) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI.Components/Controls/RecyclerView/CollectionView.cs:line 387
   at Tizen.NUI.Components.RecyclerViewItem.OnKey(Key key) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI.Components/Controls/RecyclerView/Item/RecyclerViewItem.cs:line 218
   at Tizen.NUI.ViewWrapperImpl.DirectorOnKey(IntPtr arg0) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/internal/Common/ViewWrapperImpl.cs:line 402
   at Tizen.NUI.NDalicPINVOKE.ApplicationMainLoop(HandleRef jarg1)
   at Tizen.NUI.Application.MainLoop() in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/internal/Application/Application.cs:line 1239
   at Tizen.NUI.NUICoreBackend.Run(String[] args) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/internal/Application/NUICoreBackend.cs:line 193
   at Tizen.Applications.CoreApplication.Run(String[] args) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.Applications.Common/Tizen.Applications/CoreApplication.cs:line 126
   at Tizen.NUI.NUIApplication.Run(String[] args) in /home/seoyeon/mywork/develmaster/TizenFX/src/Tizen.NUI/src/public/Application/NUIApplication.cs:line 368
   at Tizen.NUI.StyleGuide.Program.Main(String[] args) in /home/seoyeon/mywork/develmaster/TizenFX/test/Tizen.NUI.StyleGuide/Tizen.NUI.StyleGuide.cs:line 382

```

**이슈 원인 :**

 `System.EntryPointNotFoundException: Unable to find an entry point named 'feedback_initialize' in shared library 'libfeedback.so.0'.`

 Feedback 관련 라이브러리가 없어 feedback init을 할 수 없다
 > 참고로, Feedback은 Haptic 기술로써, 사용자가 디바이스를 사용했을 때, touch가 되었다는 것을 인식할 수 있게 하는 피드백 (예를 들어, 터치 시 진동 등)<br>
    Haptic feedback is the use of touch to communicate with users. Most people know the feeling of a vibration in a mobile phone or the rumble in a game controller. <br>
    NUI에는 `Control` class에 Feedback property가 있고, 이와 같이 설명하고 있다 : _Enable/Disable a sound feedback when tap gesture detected._

**해결 방안 :**

 `Switch` class에서도 이미 이것을 인지하고 있어서 Mobile profile에서만 동작하도록 Feedback property를 막아놓고 있었다.
  샘플도 동일하게 #if 구문 추가



# Unity6-StarterKit
Starter Kit for Unity6

INTRODUCTION
- Brief Project Description: Before starting a new project with Unity 6, we have gathered the necessary development assets.
- Project Goals and Direction
  - Shorten the development schedule.
  - Improve productivity by creating modules that are commonly used in game development.
  - Continuously enhance the framework to help programmers improve their skills and accumulate technical expertise.
- Rendering Pipeline: built-in, URP, HDRP
- 2D & 3D supported
- All source code, including the framework, has been made public. (no dll)
- Unity version: 6000.2.1f1
- Platform: Windows, Android
- License: MIT
- Unity Project Window screenshot:
<img width="196" height="582" alt="image" src="https://github.com/user-attachments/assets/0c7c4d00-9766-4a60-8fa9-dcb387ad80f7" />


1. Third-party plugins from Unity Asset Store(Free assets)
   1. Pools: https://assetstore.unity.com/packages/tools/utilities/pools-231438
   2. DOTween: https://assetstore.unity.com/packages/tools/animation/dotween-hotween-v2-27676
   3. In-game Debug Console: https://assetstore.unity.com/packages/tools/gui/in-game-debug-console-68068
   4. PlayerPrefs Editor: https://assetstore.unity.com/packages/tools/utilities/playerprefs-editor-167903
   5. Ultimate FPS Counter: https://assetstore.unity.com/packages/tools/gui/graphy-ultimate-fps-counter-stats-monitor-debugger-105778
   6. Serialized Dictionary: https://assetstore.unity.com/packages/tools/utilities/serialized-dictionary-243052
   7. Extenject Dependency Injection IOC: https://assetstore.unity.com/packages/tools/utilities/extenject-dependency-injection-ioc-157735
   8. Simple Scroll-Snap: https://assetstore.unity.com/packages/tools/gui/simple-scroll-snap-140884
   9.  JSON Object: https://assetstore.unity.com/packages/tools/input-management/json-object-710
   10. Singleton Pattern: https://assetstore.unity.com/packages/tools/integration/singleton-liberation-inherit-from-your-own-monobehaviour-54896
2.  Design Pattern Samples: https://github.com/Habrador/Unity-Programming-Patterns
3.  Framework
    1.  Addressables
        1.  SpriteAtlasContainer.cs
    2.  Animation
        1.  UI_AnimationPopup.cs
        2.  UI_AnimationText.cs
    3.  AssetsLoader
        1.  BaseLoader.cs
        2.  SpriteLoader.cs
        3.  TexturesLoader.cs
    4.  Audio
        1.  SoundContainer.cs
        2.  SoundController.cs
    5.  Fonts
    6.  Plugins
        1.  AssetManager
        2.  DOTWeen
        3.  Pools
        4.  Singleton
    7.  Prefabs
    8.  Scenes
    9.  Scripts
        1.  FrameworkDefine.cs
        2.  UserInfoManager.cs
    10. UI
        1.  Base
            1.  PopupBase.cs
            2.  UI_Base.cs
            3.  UI_Button.cs
            4.  UI_Manager.cs
            5.  UI_Model.cs
            6.  UI_Panel.cs
            7.  UI_Type.cs
        2.  Board
            1.  BoardFactory.cs
            2.  BoardHeaderView.cs
            3.  BoardPageController.cs
            4.  BoardPageView.cs
            5.  BoardTestData.cs
            6.  ItemViewBase.cs
            7.  ItemViewImage.cs
            8.  ItemViewText.cs
            9.  PageBoardTable.cs
            10. ScrollBoardTable.cs
            11. TableModel.cs
        3.  Popup
            1.  Dialogues
                1.  DialogueController.cs
                2.  DialogueModel.cs
                3.  DialoguePopup.cs
                4.  DialogueView.cs
            2.  Test
                1.  PopupTester.cs
            3.  ToastMessage
                1.  ToastContainer.cs
                2.  ToastMessage.cs
                3.  ToastView.cs
            4.  PopupContainer.cs
            5.  PopupFactory.cs
            6.  PopupImage.cs
            7.  PopupModel.cs
            8.  PopupNormal.cs
    11. Utils
        1.  Random
            1.  SimpleSystemRandom.cs
            2.  UnityMersenneTwister.cs
            3.  UnityNormalDistribution.cs
        2.  CommonUtils.cs

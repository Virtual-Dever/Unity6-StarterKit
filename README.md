# Unity6-StarterKit
Starter Kit for Unity6

# INTRODUCTION
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
<img width="187" height="580" alt="image" src="https://github.com/user-attachments/assets/582c5afb-d5d1-4068-910e-54507a1fe976" />

# PROPS
1. Reusability
   1. Common features (input handling, UI system, scene management, data handling, etc.) can be reused across multiple projects.
2. Faster Development
   1. Reduces repetitive coding, which shortens the development schedule.
3. Consistency
   1. Maintains a uniform code style and structure throughout the project, making collaboration easier.
4. Scalability
   1. Modular structure allows easy addition and expansion of new features.
5. Learning and Skill Accumulation
   1. Designing and implementing a framework improves programmers’ design skills and architectural understanding.
6. Fewer Bugs
   1. Reusing well-tested common code reduces the chance of errors when writing new code.

# CONS
1. High Initial Development Cost
   1. Designing and building the framework takes significant time and effort.
2. Over-generalization
   1. Trying to make it too generic can result in an unnecessarily complex structure.
3. Maintenance Burden
   1. As the framework grows, more resources are needed for bug fixes, refactoring, and documentation.
4. Learning Curve
   1. Team members may need extra time to understand the framework’s structure and rules.
5. Technical Lock-in
   1. Heavy reliance on a framework can limit flexibility when adopting new engine features or third-party libraries.
6. Mismatch with Projects
   1. Some projects may not need all the features, making the framework inefficient or excessive.

# Third-party plugins from Unity Asset Store(Free assets)
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
  

#  Design Pattern Samples:

https://github.com/Habrador/Unity-Programming-Patterns

#  Framework
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

# CODING CONVENTION GUIDE

General C# Coding Conventions  
• Classes, Structs, Interfaces: PascalCase (e.g., PlayerController, EnemyAI)  
• Methods: PascalCase (e.g., MovePlayer(), TakeDamage())  
• Variables (fields, locals): camelCase (e.g., health, playerSpeed)  
• Constants / Static readonly: ALL_CAPS_WITH_UNDERSCORES (e.g., MAX_HEALTH)  
• Private fields: prefix with _ (e.g., _health, _rigidbody)  
• Braces: Use consistent style (Allman or K&R;).  
• Indentation: 4 spaces, no tabs.  
• Comments: Use /// for XML docs, // for inline comments.  

Unity-Specific Conventions  
• Organize MonoBehaviour lifecycle methods in order: Awake, Start, Update, FixedUpdate, OnDestroy.  
• Use [SerializeField] for private fields exposed in Inspector.  
• Keep fields private unless public access is needed.  
• Organize scripts into functional folders (Gameplay, UI, Managers, Utilities).  
• Avoid magic numbers—use constants or ScriptableObjects.  
• Cache components in Awake instead of repeated GetComponent() calls.  

Example Script Structure  
• Fields (serialized and private).  
• Unity lifecycle methods (Awake, Start, Update, etc.).  
• Custom methods grouped logically.  
• Use clear naming and avoid unnecessary complexity  

Example: PlayerController Script  
```cs
using UnityEngine;  
public class PlayerController : MonoBehaviour  
{  
    [SerializeField] private float _moveSpeed = 5f;  
    [SerializeField] private int _maxHealth = 100;  
    private Rigidbody _rb;  
    private int _currentHealth;  
    private void Awake()  
    {  
    _rb = GetComponent<Rigidbody>();  
    _currentHealth = _maxHealth;  
    }  

    private void Update()
    {
        Move();
    }

    private void Move()
    {
    float h = Input.GetAxis("Horizontal");float v = Input.GetAxis("Vertical");
    Vector3 direction = new Vector3(h, 0, v).normalized;
    _rb.MovePosition(transform.position + direction * _moveSpeed * Time.deltaTime);
    }

    public void TakeDamage(int amount)
    {
        _currentHealth -= amount;
        if (_currentHealth <= 0)
        {   
            Die();
        }
    }

    private void Die()
    {
        Destroy(gameObject);
    }
}
```

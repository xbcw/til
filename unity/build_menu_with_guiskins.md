# Build a menu with GUISkin

To create a GUI Skin, select `Assets->Create->GUI Skin` from the menubar.

Here's how to build
```
    private var isPaused = false;
    var resumeTexture : Texture2D;

    function Update () {
        if(Input.GetKeyDown("escape")  !isPaused)
        {
            print("Puased");
            Time.timeScale = 0.0;
            isPaused = true;
            GetComponent(MouseLook).enabled = false;
            GameObject.Find("First Person Controller").GetComponent(MouseLook).enabled = false;
        }
        else if(Input.GetKeyDown("escape")  isPaused)
        {
            print("Unpuased");
            Time.timeScale = 1.0;
            isPaused = false;
            GetComponent(MouseLook).enabled = true;
            GameObject.Find("First Person Controller").GetComponent(MouseLook).enabled = true;
        }
    }
    //Create and check if the buttons are being pressed.
    function OnGUI(){
        if(isPaused)
        {
            if(GUI.Button (Rect((Screen.width-140)/2,80,140,70), resumeTexture, GUIStyle.none))
            {
                print("Quit!");
                //Application.Quit();
            }
            if(GUI.Button (Rect((Screen.width-140)/2,200,140,70), resumeTexture, GUIStyle.none))
            {
                print("Restart");
                Application.LoadLevel("UnitySpelprojekt");
                Time.timeScale = 1.0;
                isPaused = false;
            }
            if(GUI.Button (Rect((Screen.width-140)/2,280,140,70), resumeTexture, GUIStyle.none))
            {
                print("Continue");
                Time.timeScale = 1.0;
                isPaused = false;
                GetComponent(MouseLook).enabled = true;
                GameObject.Find("First Person Controller").GetComponent(MouseLook).enabled = true;
            }
        }
    }

```

[source](http://docs.unity3d.com/Manual/class-GUISkin.html)
# Capacitor Check App Update
_Check the App and Play store for app updates!_

### Installation
```shell script
npm install --save @abitofsoftware/capacitor-check-app-update
```

#### Android
Add the plugin to the MainActivity in the Android project
```
import com.abitofsoftware.checkappupdate.CheckAppUpdatePlugin;

public class MainActivity extends BridgeActivity {
  @Override
  public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);

    // Initializes the Bridge
    this.init(savedInstanceState, new ArrayList<Class<? extends Plugin>>() {{
      // Additional plugins you've installed go here
      add(CheckAppUpdatePlugin.class);
    }});
  }
}
```

### Usage
```angularjs
import {CheckAppUpdate} from "@abitofsoftware/capacitor-check-app-update";
const checkAppUpdate = new CheckAppUpdate();

checkAppUpdate.canUpdate()
    .then({value: boolean} => {
        if(value) {
            // ... prompt user to update
        }    
    })
```

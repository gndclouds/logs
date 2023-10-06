---
title: Arena Frame
publishedAt:
type:
  - Note
published: true
tags: physical-computing
---


Sure, creating an app for your Raspberry Pi and its HyperPixel display that interfaces with the Are.na API sounds like an exciting project. Here's a basic outline to get you started:

### Prerequisites:

1. Raspberry Pi with Raspbian OS.
2. HyperPixel display set up.
3. Python installed (it usually comes preinstalled on Raspbian).

### Steps:

1. **Setup the Environment**:
   - You'll need to install the necessary libraries. You can use `pip` for this.
     ```
     pip3 install requests kivy
     ```

2. **Fetch Data from Are.na API**:
   - You'll use the `requests` library to fetch data from your Are.na channel.

3. **GUI with Kivy**:
   Kivy is a popular Python library for creating GUIs on the Raspberry Pi.

   ```python
   from kivy.app import App
   from kivy.uix.boxlayout import BoxLayout
   import requests

   class ArenaApp(App):

       def build(self):
           self.data = self.get_arena_data()
           self.index = 0
           layout = BoxLayout()
           # Populate layout with the first block of data from your channel
           # Add touch event handlers
           return layout

       def get_arena_data(self):
           # Use requests to get data from your Are.na channel
           response = requests.get('ARE.NA_API_URL_HERE')
           data = response.json()
           return data['blocks']

       def on_touch_down(self, touch):
           if touch.x < self.width/3:  # Touch on left
               self.index -= 1
           elif touch.x > 2*self.width/3:  # Touch on right
               self.index += 1
           else:  # Touch in center
               # Display popup to switch channels
               pass

           # Update display based on new index

   ArenaApp().run()
   ```

   Note: Replace `'ARE.NA_API_URL_HERE'` with the appropriate Are.na API endpoint for your channel.

4. **Add Popup for Channel Switching**:
   - You can use Kivy’s `Popup` widget to show a popup where users can switch channels.

5. **Handling Touch**:
   - Use the `on_touch_down` method to detect touch events and determine which third of the screen was touched to either switch blocks or display the popup.

6. **Auto-Start on Boot**:
   If you want the app to automatically start when the Raspberry Pi boots up, you can edit the `.bashrc` file:
   ```
   echo "python3 /path_to_your_script/script_name.py" >> ~/.bashrc
   ```

7. **Full-Screen Mode**:
   To make your app run in full-screen mode on Kivy, you can modify the `~/.kivy/config.ini` file and set the height and width to match your HyperPixel display's resolution and set fullscreen to `1`.

Remember, this is a basic outline, and you'll need to fill in details specific to your application and Are.na channel structure. You might also want to implement error handling, especially when dealing with network requests.

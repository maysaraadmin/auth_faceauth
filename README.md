Moodle Face Authentication Plugin
This Moodle plugin integrates a facial recognition authentication system into your Moodle login process. The plugin uses webcam capture to verify users' identities before granting access to the Moodle platform. It provides an additional layer of security by enabling users to authenticate using their faces.

Features
Webcam Integration: Allows users to authenticate using their webcam.
Face Capture: Users can capture a snapshot of their face for authentication.
Retry Option: If the first attempt fails, users can retry the capture.
Message Display: Provides success or error messages for user feedback.
Loader: Displays a loading message during the authentication process.
Responsive Design: Optimized for both desktop and mobile views.
Installation
1. Clone or Download the Plugin
Clone or download the plugin to your Moodle instance's auth directory. You can do this by running the following command in your Moodle root directory:

bash
Copy code
git clone https://github.com/yourusername/moodle-auth-faceauth.git auth/faceauth
2. Install the Plugin
Navigate to your Moodle site's administration page.
Go to Site administration > Notifications.
Moodle will automatically detect the new plugin and prompt you to install it.
Follow the on-screen instructions to complete the installation.
3. Enable the Plugin
After installation, go to Site administration > Plugins > Authentication > Manage authentication.
Find the Face Authentication plugin in the list and enable it.
4. Add the JavaScript and CSS Files
The plugin includes the necessary JavaScript and CSS files for facial recognition functionality. These are automatically added to the page by the plugin, but you can ensure they’re included by adding the following lines in the login/index.php file:

php
Copy code
$PAGE->requires->js('/auth/faceauth/faceauth.js');  // Include your custom JS for facial recognition
$PAGE->requires->css('/auth/faceauth/style.css');   // Include the CSS for styling
5. Configure the Plugin
You may configure additional settings (such as webcam resolution and timeout durations) by editing the plugin configuration page.

Usage
How to Use Face Authentication
Once the plugin is enabled, users can authenticate using the following steps:

Login Page: On the login page, a video feed will appear. This feed is from the user's webcam.
Capture Face: Users can click the Capture Face button to take a snapshot of their face.
Retry Option: If the face capture fails, users can click the Retry button to try again.
Submit: After a successful capture, users can click Submit to send their face data to the server for authentication.
Success/Failure: Once the submission is processed, users will be notified whether the face was successfully enrolled or if there was an issue with the capture.
User Interface Elements
Video: Displays a live feed from the webcam for capturing the face.
Canvas: Holds the captured image (invisible during normal operation).
Image Preview: Displays a preview of the captured face image.
Buttons:
Capture Face: Triggers the face capture action.
Retry: Allows the user to retry capturing their face.
Submit: Submits the captured face for authentication.
Loader: Shows a loading message while the submission is processed.
Message Box: Displays success, error, or informational messages.
Contributing
We welcome contributions to this plugin. If you have suggestions, bug fixes, or improvements, feel free to submit a pull request or open an issue.

How to Contribute
Fork the repository to your own GitHub account.
Clone the forked repository to your local machine.
Make changes or fixes.
Push the changes to your forked repository.
Create a pull request to the main repository.
Issues and Bugs
If you encounter any issues, please open an issue on GitHub. Be sure to include the steps to reproduce the issue and any relevant error messages.

License
This plugin is licensed under the MIT License.

Acknowledgments
Thanks to the Moodle Community for providing the framework and support for this plugin.
The facial recognition logic is powered by Face API.

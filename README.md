# Mac Setup M2

Install X Code via AppleScript:

------Begin Paste------
xcode-select --install > /dev/null 2>&1
if [ 0 == $? ]; then
    sleep 1
    osascript <<EOD
tell application "System Events"
    tell process "Install Command Line Developer Tools"
        keystroke return
        click button "Agree" of window "License Agreement"
    end tell
end tell
EOD
else
    echo "Command Line Developer Tools are already installed!"
fi
------End Paste------

Install Homebrew:

Setup for new Mac - Corporate



Setup for new Mac - Personal

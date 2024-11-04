import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.io.BufferedReader;
import java.io.InputStreamReader;
 

public class PCControlApp {

    public static void main(String[] args) {
        // Set up the frame
        JFrame frame = new JFrame("PC Control Application");
        frame.setSize(400, 300);  // Increased size for better visibility
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // Set up components
        JTextField commandField = new JTextField(25);  // For typing commands
        JButton executeButton = new JButton("Execute Command");
        JTextArea outputArea = new JTextArea(10, 30);
        outputArea.setEditable(false);  // Set output area as read-only

        // Add components to the frame
        JPanel panel = new JPanel();
        panel.add(new JLabel("Enter Command:"));
        panel.add(commandField);
        panel.add(executeButton);
        frame.add(panel, "North");
        frame.add(new JScrollPane(outputArea), "Center");

        // Add action listener for the button
        executeButton.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                String command = commandField.getText();
                if (!command.isEmpty()) {
                    String result = executeCommand(command);
                    outputArea.setText(result);  // Display the output
                } else {
                    outputArea.setText("Please enter a command.");
                }
            }
        });

        // Display the frame
        frame.setVisible(true);
    }

    // Method to execute system commands and open applications
    private static String executeCommand(String command) {
        StringBuilder output = new StringBuilder();
        Process process;

        try {
            // Detect OS
            String os = System.getProperty("os.name").toLowerCase();
            String url;

            // Internal Commands
            switch (command.toLowerCase()) {
                case "open powerpoint":
                    process = executeInternalCommand(os, "cmd /c start powerpnt");
                    break;
                case "open word":
                    process = executeInternalCommand(os, "cmd /c start winword");
                    break;
                case "open excel":
                    process = executeInternalCommand(os, "cmd /c start excel");
                    break;
                case "open notepad":
                    process = executeInternalCommand(os, "cmd /c start notepad");
                    break;
                case "open camera":
                    process = executeInternalCommand(os, "cmd /c start microsoft.windows.camera:");
                    break;
                case "open whatsapp":
                    process = executeInternalCommand(os, "cmd /c start whatsapp:");
                    break;
                case "open vlc":
                    process = executeInternalCommand(os, "cmd /c start vlc");
                    break;
                case "open paint":
                    process = executeInternalCommand(os, "cmd /c start mspaint");
                    break;
                case "open file explorer":
                    process = executeInternalCommand(os, "cmd /c start explorer");
                    break;
                case "open task manager":
                    process = executeInternalCommand(os, "cmd /c start taskmgr");
                    break;
                case "open cmd":
                    process = executeInternalCommand(os, "cmd /c start cmd");
                    break;
                case "open settings":
                    process = executeInternalCommand(os, "cmd /c start ms-settings:");
                    break;
                case "open adobe reader":
                    process = executeInternalCommand(os, "cmd /c start acrord32");
                    break;
                case "open spotify":
                    process = executeInternalCommand(os, "cmd /c start spotify");
                    break;
                case "open discord":
                    process = executeInternalCommand(os, "cmd /c start discord");
                    break;
                case "open steam":
                    process = executeInternalCommand(os, "cmd /c start steam");
                    break;
                case "open task scheduler":
                    process = executeInternalCommand(os, "cmd /c start taskschd.msc");
                    break;
                case "open device manager":
                    process = executeInternalCommand(os, "cmd /c start devmgmt.msc");
                    break;
                case "open control panel":
                    process = executeInternalCommand(os, "cmd /c start control");
                    break;
                case "open snipping tool":
                    process = executeInternalCommand(os, "cmd /c start SnippingTool");
                    break;
                case "open calculator":
                    process = executeInternalCommand(os, "cmd /c start calc");
                    break;
                case "open magnifier":
                    process = executeInternalCommand(os, "cmd /c start magnify");
                    break;
                case "open sticky notes":
                    process = executeInternalCommand(os, "cmd /c start StikyNot.exe");
                    break;
                case "open voice recorder":
                    process = executeInternalCommand(os, "cmd /c start voice.exe");
                    break;
                case "open ms paint":
                    process = executeInternalCommand(os, "cmd /c start mspaint");
                    break;
                case "open map":
                    process = executeInternalCommand(os, "cmd /c start ms-maps:");
                    break;
                case "open powershell":
                    process = executeInternalCommand(os, "cmd /c start powershell");
                    break;
                case "open chrome":
                    process = executeInternalCommand(os, "cmd /c start chrome");
                    break;
                case "open firefox":
                    process = executeInternalCommand(os, "cmd /c start firefox");
                    break;
                case "open edge":
                    process = executeInternalCommand(os, "cmd /c start msedge");
                    break;
                case "open onenote":
                    process = executeInternalCommand(os, "cmd /c start onenote");
                    break;
                case "open outlook":
                    process = executeInternalCommand(os, "cmd /c start outlook");
                    break;
                case "open teams":
                    process = executeInternalCommand(os, "cmd /c start teams");
                    break;
                case "open ms store":
                    process = executeInternalCommand(os, "cmd /c start ms-windows-store:");
                    break;
                case "open appskype":
                    process = executeInternalCommand(os, "cmd /c start skype:");
                    break;
                case "open java":
                    process = executeInternalCommand(os, "cmd /c start javaw");
                    break;
                case "open git bash":
                    process = executeInternalCommand(os, "cmd /c start bash");
                    break;
                case "open git gui":
                    process = executeInternalCommand(os, "cmd /c start git-gui");
                    break;
                case "open eclipse":
                    process = executeInternalCommand(os, "cmd /c start eclipse");
                    break;
                case "open netbeans":
                    process = executeInternalCommand(os, "cmd /c start netbeans");
                    break;
                case "open visual studio":
                    process = executeInternalCommand(os, "cmd /c start devenv");
                    break;
                case "open android studio":
                    process = executeInternalCommand(os, "cmd /c start studio64");
                    break;
                case "open roblox":
                    process = executeInternalCommand(os, "cmd /c start RobloxPlayerBeta");
                    break;
                case "open fortnite":
                    process = executeInternalCommand(os, "cmd /c start Fortnite");
                    break;
                case "open minecraft":
                    process = executeInternalCommand(os, "cmd /c start Minecraft");
                    break;
                case "open bluestacks":
                    process = executeInternalCommand(os, "cmd /c start Bluestacks");
                    break;
                // Web Commands
                case "open google":
                    process = executeWebCommand(os, "https://www.google.com");
                    break;
                case "open instagram":
                    process = executeWebCommand(os, "https://www.instagram.com");
                    break;
                case "open facebook":
                    process = executeWebCommand(os, "https://www.facebook.com");
                    break;
                case "open youtube":
                    process = executeWebCommand(os, "https://www.youtube.com");
                    break;
                case "open drive":
                    process = executeWebCommand(os, "https://drive.google.com");
                    break;
                case "open google sheets":
                    process = executeWebCommand(os, "https://sheets.google.com");
                    break;
                case "open google slides":
                    process = executeWebCommand(os, "https://slides.google.com");
                    break;
                case "open twitter":
                    process = executeWebCommand(os, "https://www.twitter.com");
                    break;
                case "open linkedin":
                    process = executeWebCommand(os, "https://www.linkedin.com");
                    break;
                case "open pinterest":
                    process = executeWebCommand(os, "https://www.pinterest.com");
                    break;
                case "open reddit":
                    process = executeWebCommand(os, "https://www.reddit.com");
                    break;
                case "open stack overflow":
                    process = executeWebCommand(os, "https://stackoverflow.com");
                    break;
                case "open quora":
                    process = executeWebCommand(os, "https://www.quora.com");
                    break;
                case "open ebay":
                    process = executeWebCommand(os, "https://www.ebay.com");
                    break;
                case "open amazon":
                    process = executeWebCommand(os, "https://www.amazon.com");
                    break;
                case "open netflix":
                    process = executeWebCommand(os, "https://www.netflix.com");
                    break;
                case "open hulu":
                    process = executeWebCommand(os, "https://www.hulu.com");
                    break;
                case "open webspotify":
                    process = executeWebCommand(os, "https://www.spotify.com");
                    break;
                case "open soundcloud":
                    process = executeWebCommand(os, "https://www.soundcloud.com");
                    break;
                case "open bbc":
                    process = executeWebCommand(os, "https://www.bbc.com");
                    break;
                case "open cnn":
                    process = executeWebCommand(os, "https://www.cnn.com");
                    break;
                case "open al jazeera":
                    process = executeWebCommand(os, "https://www.aljazeera.com");
                    break;
                case "open ny times":
                    process = executeWebCommand(os, "https://www.nytimes.com");
                    break;
                case "open forbes":
                    process = executeWebCommand(os, "https://www.forbes.com");
                    break;
                case "open wikihow":
                    process = executeWebCommand(os, "https://www.wikihow.com");
                    break;
                case "open coursera":
                    process = executeWebCommand(os, "https://www.coursera.org");
                    break;
                case "open udemy":
                    process = executeWebCommand(os, "https://www.udemy.com");
                    break;
                case "open khan academy":
                    process = executeWebCommand(os, "https://www.khanacademy.org");
                    break;
                case "open edx":
                    process = executeWebCommand(os, "https://www.edx.org");
                    break;
                case "open codecademy":
                    process = executeWebCommand(os, "https://www.codecademy.com");
                    break;
                case "open freecodecamp":
                    process = executeWebCommand(os, "https://www.freecodecamp.org");
                    break;
                case "open leetcode":
                    process = executeWebCommand(os, "https://www.leetcode.com");
                    break;
                case "open codewars":
                    process = executeWebCommand(os, "https://www.codewars.com");
                    break;
                case "open hackerrank":
                    process = executeWebCommand(os, "https://www.hackerrank.com");
                    break;
                case "open gitHub":
                    process = executeWebCommand(os, "https://www.github.com");
                    break;
                case "open bitbucket":
                    process = executeWebCommand(os, "https://bitbucket.org");
                    break;
                case "open jira":
                    process = executeWebCommand(os, "https://www.atlassian.com/software/jira");
                    break;
                case "open trello":
                    process = executeWebCommand(os, "https://trello.com");
                    break;
                case "open slack":
                    process = executeWebCommand(os, "https://slack.com");
                    break;
                case "open zoom":
                    process = executeWebCommand(os, "https://zoom.us");
                    break;
                case "open teamviewer":
                    process = executeWebCommand(os, "https://www.teamviewer.com");
                    break;
                case "open skype":
                    process = executeWebCommand(os, "https://www.skype.com");
                    break;
                case "open hangouts":
                    process = executeWebCommand(os, "https://hangouts.google.com");
                    break;
                case "open meet":
                    process = executeWebCommand(os, "https://meet.google.com");
                    break;
                case "open vimeo":
                    process = executeWebCommand(os, "https://www.vimeo.com");
                    break;
                case "open dailymotion":
                    process = executeWebCommand(os, "https://www.dailymotion.com");
                    break;
                case "open twitch":
                    process = executeWebCommand(os, "https://www.twitch.tv");
                    break;
                case "open behance":
                    process = executeWebCommand(os, "https://www.behance.net");
                    break;
                case "open deviantart":
                    process = executeWebCommand(os, "https://www.deviantart.com");
                    break;
                case "open dribbble":
                    process = executeWebCommand(os, "https://www.dribbble.com");
                    break;
                case "open 500px":
                    process = executeWebCommand(os, "https://500px.com");
                    break;

                default:
                    output.append("Command not recognized.");
                    return output.toString();
            }

            // Check for successful process execution
            BufferedReader reader = new BufferedReader(new InputStreamReader(process.getInputStream()));
            String line;
            while ((line = reader.readLine()) != null) {
                output.append(line).append("\n");
            }
            process.waitFor();
            reader.close();

        } catch (Exception e) {
            output.append("Error executing command: ").append(e.getMessage());
        }

        return output.toString();
    }

    // Method to execute internal commands based on the OS
    private static Process executeInternalCommand(String os, String command) throws Exception {
        if (os.contains("win")) {
            return Runtime.getRuntime().exec(command);
        } else if (os.contains("mac")) {
            return Runtime.getRuntime().exec(new String[]{"/usr/bin/open", "-a", command});
        } else {
            return Runtime.getRuntime().exec(command);
        }
    }

    // Method to open a web URL
    private static Process executeWebCommand(String os, String url) throws Exception {
        if (os.contains("win")) {
            return Runtime.getRuntime().exec(new String[]{"cmd", "/c", "start", url});
        } else if (os.contains("mac")) {
            return Runtime.getRuntime().exec(new String[]{"/usr/bin/open", url});
        } else {
            return Runtime.getRuntime().exec(new String[]{"xdg-open", url});
        }
    }
}

# Switching Between Meshery Release Channels: A Guide

Meshery is a versatile service mesh management platform, and to ensure that users get the best possible experience, it has two distinct release channels: stable and edge. These channels allow users to choose between a thoroughly tested, production-ready version of Meshery, or the latest features and improvements that may come with more instability.

In this guide, we'll explain the difference between these two channels, and show you how to switch between them using the mesheryctl command-line tool, editing the meshconfig file, or through the Meshery UI.

* Understanding the Two Release Channels: The stable channel is the most thoroughly tested version of Meshery and is considered to be production-ready. This channel is recommended for users who value stability and reliability over the latest features.
    

On the other hand, the edge channel provides the latest features and improvements as they are developed, but may not have undergone the same level of testing as the stable channel. This channel is recommended for users who want to take advantage of the latest advancements, and are prepared to deal with any bugs that may arise.

Switching Channels with mesheryctl: The simplest way to switch between channels is to use the *mesheryctl* command-line tool. To switch to the stable channel, run the following command:

```python
mesheryctl channel set stable
```

And to switch to the edge channel, run this command:

```python
mesheryctl channel set edge
```

* Switching Channels by Editing meshconfig: You can also switch channels by editing the *meshconfig* file, which is located in your home directory and named *.meshery/meshconfig.yaml****.*** Open this file in a text editor and locate the following line:
    
    ```makefile
    channel: stable
    ```
    

Change the word "stable" to "edge" to switch to the edge channel, then save the file and restart Meshery for the changes to take effect.

* Confirming the Channel Switch: Finally, you can confirm that you have successfully switched channels by checking the Meshery UI, running the mesheryctl version command, or by viewing the mesheryctl system channel.
    

In the Meshery UI, go to the System page, and you should see the Channel field display either **"Stable" or "Edge"**.

To check the channel using mesheryctl version command, simply run the following in your terminal:

```bash
mesheryctl version
```

The output should include a line that reads "**Channel**: **stable" or "Channel: edge"**, depending on which channel you have switched to.

Finally, to view the mesheryctl system channel, run the following command:

```sql
mesheryctl system channel view
```

This will display the current channel, and provide a clear indication of whether you have successfully switched channels or not.

In conclusion, switching between Meshery release channels is a straightforward process, and allows you to choose the version of Meshery that best suits your needs. Whether you prioritize stability and reliability or want to take advantage of the latest features and improvements, Meshery provides the flexibility to do so.
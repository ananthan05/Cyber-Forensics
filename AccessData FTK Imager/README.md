# Tutorial on AccessData FTK Imager

## Disk Imaging using FTK Imager ##

### Description of the tool ###


A forensic imaging programme is called FTK Imager, or Forensic Toolkit Imager. It is frequently used to produce forensic photographs of storage devices, including hard discs, USB drives, and other media, in the field of digital forensics. By making a bit-by-bit replica of a storage device's whole contents, forensic imaging helps to minimise any alterations or damage while maintaining the original data for examination.


Important UI elements that are essential to FTK Imager's operation are included. These elements consist of:

- **Evidence Tree Pane**: Shows forensic picture files, hard drives, and flash drives as additional evidence sources in a hierarchical format.
- **File List Pane:** From the Evidence Tree Pane, this pane shows a list of files and folders that are located in the directory that you have selected.
- **Viewer Pane:** Shows the contents of the chosen files in the File List Pane or the Evidence Tree Pane.


![Screenshot 2024-02-11 201357](https://github.com/anandurdas11/CyberForensics/assets/83402050/43caa0f9-b786-4a98-af39-3d9f58834e80)


### Adding the evidence item ###

Open **FTK Imager** and navigate to `File > Add Evidence Item`

![Screenshot 2024-02-11 201510](https://github.com/anandurdas11/CyberForensics/assets/83402050/7fc3aa50-f509-4b1b-bab6-302b351759cd)


Choose **Physical Drive** on the **Select Source** window, then click **Next**.

![Screenshot 2024-02-11 201640](https://github.com/anandurdas11/CyberForensics/assets/83402050/ada22243-d058-4d4f-b55d-0e1c5b1ef7c0)


Choose **Microsoft Virtual Disk** (our virtual flash drive) on the **Select Drive** window, then click **Finish**.

![Screenshot 2024-02-11 201727](https://github.com/anandurdas11/CyberForensics/assets/83402050/d9126844-1fe6-470e-aa42-361aa07f7deb)


Navigate and click `File > Detect EFS Encryption` to scan the drive and detect the presence of encryption.

![Screenshot 2024-02-11 201810](https://github.com/anandurdas11/CyberForensics/assets/83402050/354500c3-8b08-449b-9332-1d9b8e699e46)

A message box will indicate whether or not EFS encryption is on the attached drive.

![Screenshot 2024-02-11 201843](https://github.com/anandurdas11/CyberForensics/assets/83402050/72442517-2675-4087-9c97-63ea630c6875)


### Creating a Forensic Disk Image with FTK Imager ###

Open **FTK Imager** and navigate to `File > Create Disk Image`

![Screenshot 2024-02-11 202019](https://github.com/anandurdas11/CyberForensics/assets/83402050/803481e2-f394-4f8c-b354-cd204ff431f3)


Choose **Physical Drive** on the **Select Source** window, then click **Next**.

![Screenshot 2024-02-11 202035](https://github.com/anandurdas11/CyberForensics/assets/83402050/a7d2035f-9f59-4801-a726-9e1ed52540e3)


Select the disk to make the image.

![Screenshot 2024-02-11 202139](https://github.com/anandurdas11/CyberForensics/assets/83402050/92cc005c-2255-48d5-849f-4b278b5b7c1f)


Ensure you check **"Verify images after they are created"** and **"Create directory listings of all files in the image after they are created"** on the **Create Image** window. Press **Add** to open the **Select Image Type** window, choose **Raw (dd)**, then click **Next**.

![Screenshot 2024-02-11 202207](https://github.com/anandurdas11/CyberForensics/assets/83402050/d7807e84-b6fa-4ab3-bd64-825b6c4f0a0d)


Enter case details in the **Evidence Item Information** window, then click **Next**.

![Screenshot 2024-02-11 202236](https://github.com/anandurdas11/CyberForensics/assets/83402050/eb4f2c0d-ca55-4f83-b355-795e7c243216)


Enter the **Image Destination Folder** and **Image Filename**, then click **Finish**.

![Screenshot 2024-02-11 202305](https://github.com/anandurdas11/CyberForensics/assets/83402050/f1ca28be-2af3-4637-b027-ce4faad51a59)


Press **Start** to begin creating the _forensic disk image_.

![Screenshot 2024-02-11 202335](https://github.com/anandurdas11/CyberForensics/assets/83402050/3ee6746e-2589-44fd-ae14-49d4f85d81d1)


![Screenshot 2024-02-11 202349](https://github.com/anandurdas11/CyberForensics/assets/83402050/9fb8a2f8-d7e0-4e0e-a99e-0a7dcea25d32)


It will start building the disk image after that we can analyze the content of the  disk.

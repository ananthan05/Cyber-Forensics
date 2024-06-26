# Imagine you're a digital forensic analyst working on a case involving a USB pendrive suspected to contain crucial evidence. Detail the steps you would take to acquire the evidence and recover files from the pendrive using the following tools: Guymager for creating a dd file, and Foremost for file recovery. Explain each step of the process, from connecting the pendrive to your forensic workstation to generating a dd file using Guymager, and then recovering files using foremost.

FIRST We would insert our usb drive.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/e0015251-0fe7-47fa-a975-3d2d93f13ca1)

Then i am going to delete the  `cat image` from this usb.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/b3db4047-6f03-4fb4-8585-49e51efc197f)

press `Delete`

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/85d1f2d3-e3fc-4cdc-b70c-b9debe36406c)

Now i amgoing to create a disk image using Guymager.

## Guymager for creating a dd file

Now we run `guymager` in our Kali Linux system. To run this tool we simply use guymager command in our terminal window.

```
sudo guymager
```
Providing command will open it's window as following:

in that will specify all the disk connected to the device.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/7f40c9ec-ea36-4660-b891-61d5b1af82ea)

Here we can see that we can clone the pen drive on our hard disks or any other flash drives. To acquire image we need to right click on the disk and select the acquire option.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/916ed9e6-6f37-49b0-b8b5-146124be512c)

And a new window will pop up.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/ba6a96b7-5bc2-40d5-8f08-c2a281de1e79)

Here we can choose the file format and provide the case number and evidence number, examiner, descriptions and notes. Here we can also choose the image directory. We can also split the size of disk. We can calculate MD% and SHA1 and SHA-256. Then we must check the verification process, because if the image acquisition was not valid then it can't be an evidence. So verification is a good habit. Here we have done everything, and set the acquired image directory in our desktop, and we did not used the split image because we are not acquiring large image. Following screenshot shows the process.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/bd6aa593-189d-4d62-91a8-1bdbb07ed7f1)

Then we just click on start option and the process will started.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/1a83d62a-8623-41cf-b1ae-9b8ffd8bae9c)

After finishing this process we will get a dd image file in our Desktop.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/98eddc4f-840d-4648-b396-07efdb9a5984)

now we will use dd image to recover the image by using `Foremost` tool

## Foremost for file recovery

Install Foremost

If Foremost is not already installed on your system, you can install it using the package manager of your operating system.

```
sudo apt-get install foremost
```

Run Foremost:

Once Foremost is successfully started, a Terminal opens, displaying the program version, creators, and some of the many switches for usage:

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/a87e7139-1d78-4a11-96df-eab1299998c6)

To have a better understanding of Foremost and the switches used, try browsing the Foremost System Manager's Manual.This can be done by entering the following command:

```
man foremost
```

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/381bfec4-a5b8-4c0a-abf1-89d2d30dbdbc)

The syntax for using Foremost is as follows:

```
foremost -i (forensic image) -o (output folder) -options
```

To recover the jpg image from  from the dd image file, use the following command syntax:

```
foremost -t jpg -i <input_file> -o <output_directory>

```

> `-t` jpg: This option specifies that Foremost should only recover JPG (JPEG) files.

> `<input_file>`: Replace this with the path to your dd image file.

>`<output_directory>`: Replace this with the directory where you want the recovered JPG images to be saved.

>This command will instruct Foremost to scan the dd image file for JPG images and recover them to the specified output directory.


![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/543ebe7d-6225-45e8-9765-5b4323655fb5)

Recovery completed. NOW go to Desktop and check whether there is a file named  `Recover`  present or not.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/c7a422e6-46e4-426b-8292-55f9b18c6c94)

Now open and check wheather  the `cat image`  is recoverd or not.

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/4d55cdb6-fafb-48e6-804d-bb63c5e44955)

Our  `cat image` has successfully recovered using `Foremost` tool.




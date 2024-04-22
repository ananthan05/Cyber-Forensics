## Below Commands will use the Volatility tool to analyze malware sample in memory dump. 

```
python3 vol.py -f sample.vmem windows.pstree
```
### 1. Install Volatility Tool by extracting tar file 
```
sudo tar -xvzf volatility3new.tar.gz
```

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/e6a16272-462c-45ab-9486-8f0dfa24e5e2)

### 2. Extract vol.py code from git repo.

```
sudo git clone https://github.com/volatilityFoundation/volatility3.git
```

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/c1f750cd-8392-4a83-b458-7fe6b43d9166)


### 3. Perform Malware Analysis using Volatility tool

```
python3 vol.py -f sample.vmem windows.pstree
```

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/b9bf7655-a188-4f74-bdee-1ec244a9b5ea)

![image](https://github.com/ananthan05/Cyber-Forensics/assets/140697378/ed9cba46-7b95-4558-8a14-339773da8ceb)

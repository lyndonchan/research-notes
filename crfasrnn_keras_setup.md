crfasrnn_keras Windows Setup
1. Install Cygwin Portable
2. Install Python3, Pip3 in Cygwin
3. Setup Python3 in Cygwin
4. Clone crfasrnn_keras into cygwin\home\root
5. Download pre-trained model weights and place in the crfasrnn_keras directory
7. Run
	patch < 3.5-issue21085-struct_siginfo.patch
6. Run following commands to install Python packages
	pip install tensorflow
	pip install tensorflow-gpu
	pip install keras
	pip install h5py
	pip install Pillow
	
Win-builds
	
	
crfasrnn_keras Windows Setup Attempt #2
1. Install MinGW (no admin privileges required), basic and C++ installations selected
2. Open MinGW command prompt
3. Run
	
# Tensorflow Errors
1. "CXXABI_1.3.8 not found" in tensorflow-gpu
Methods to solve this problem :
    1. conda update libgcc
       this will require downgrading "due to dependency conflicts" next time you update anaconda.
    2. mask the anaconda libstdc++ so that your systems's libstdc++ is used:
     ```
       cd ~/anaconda3/lib
       mv libstdc++.so libstdc++.so.bkp
       mv libstdc++.so.6 libstdc++.so.6.bkp
      ```
      you can further(optionally) create a softlink inside the anaconda lib directly
     > ln -s /usr/lib/x86_64-linux-gnu/libstdc++.so.6 libstdc++.so.6  


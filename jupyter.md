Jupyter kernal is not strating after installing the anaconda in Ubuntu 16.04


```
the error was as below:
[I 12:47:09.993 NotebookApp] Accepting one-time-token-authenticated connection from 127.0.0.1
[I 12:47:25.534 NotebookApp] Kernel started: dee8857d-6d34-4182-a33b-0d26df67049a
/home/pritesh/anaconda3/bin/python: No module named ipykernel_launcher
[I 12:47:28.534 NotebookApp] KernelRestarter: restarting kernel (1/5)
/home/pritesh/anaconda3/bin/python: No module named ipykernel_launcher
[I 12:47:31.541 NotebookApp] KernelRestarter: restarting kernel (2/5)
/home/pritesh/anaconda3/bin/python: No module named ipykernel_launcher
[I 12:47:34.545 NotebookApp] KernelRestarter: restarting kernel (3/5)
/home/pritesh/anaconda3/bin/python: No module named ipykernel_launcher
[W 12:47:35.685 NotebookApp] Timeout waiting for kernel_info reply from dee8857d-6d34-4182-a33b-0d26df67049a
[I 12:47:37.552 NotebookApp] KernelRestarter: restarting kernel (4/5)
WARNING:root:kernel dee8857d-6d34-4182-a33b-0d26df67049a restarted
```

__Solution__
reinstall the ipykernel
```
pip uninstall ipykernel
pip install ipykernel
```

# Dynamic Compression in IIS 7

For IIS7.5, an alternate method to enable compression is to run the following commands in a terminal:To enable compression for both dynamic and static content:C:\Windows\System32\Inetsrv\Appcmd.exe set config -section:urlCompression -doStaticCompression:true -doDynamicCompression:true...
For IIS7.5, an alternate method to enable compression is to run the following commands in a terminal:

To enable compression for both dynamic and static content:

```cpp
C:\Windows\System32\Inetsrv\Appcmd.exe set config -section:urlCompression -doStaticCompression:true -doDynamicCompression:true 
```

To set the compression level to 7 for dynamic, and 9 for static content:

```cpp
C:\Windows\System32\Inetsrv\Appcmd.exe set config -section:httpCompression -[name='gzip'].staticCompressionLevel:9 -[name='gzip'].dynamicCompressionLevel:7 
```

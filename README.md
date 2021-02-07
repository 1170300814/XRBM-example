# XRBM-example
python module xrbm example


1. if install xrbm fault. try to uninstall setuptools then try again!
2. if "Unknown MS Compiler version 1900" fail. 
  1> YOU can download "https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win64/Personal%20Builds/mingw-builds/8.1.0/threads-posix/seh/x86_64-8.1.0-release-posix-seh-rt_v6-rev0.7z" (it is mingw) .  
  2> then add the bin folder path to the computer environment.  
  3> In anaconda under the "Anaconda3\Lib\distutils" search cygwinccompiler.py. Change   
       > elif msc_ver == '1600':  
       >># VS2010 / MSVC 10.0  
        >>>  return ['msvcr100']  
    TO  
       > elif msc_ver == '1600':  
           >> # VS2010 / MSVC 10.0  
           >>> return ['msvcr100']  
       > elif msc_ver == '1700':  
         >>   # Visual Studio 2012 / Visual C++ 11.0  
          >>>  return ['msvcr110']  
       > elif msc_ver == '1800':  
           >> # Visual Studio 2013 / Visual C++ 12.0  
          >>>  return ['msvcr120']  
       > elif msc_ver == '1900':  
          >>  # Visual Studio 2015 / Visual C++ 14.0  
           >> # "msvcr140.dll no longer exists" http://blogs.msdn.com/b/vcblog/archive/2014/06/03/visual-studio-14-ctp.aspx  
          >>>  return ['vcruntime140']  
            
    
    
3. if tensorflow put a fault "module 'tensorflow' has no attribute 'contrib' ".Because tensorflow 2.x has removed the module contrib,you should install tensorflow 1.x
          

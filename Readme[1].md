## How to use:
## 
The executable will create required folders as long as it has permissions in the directory it is running from (default config).

The input file needs to be placed in 'Input' folder. Once processed the file is moved to 'Input\Processed'. If it fails then it is moved to 'Input\Failed'.

The output report is created in 'Output' folder.

The processed, failed and output files have timestamp appended to them to avoid duplicates.


## Libraries Used:
## 
All libraries used are from NuGet

1) AutoMapper

2) Castle.Core

3) Castle.Core-log4net

4) Castle.LoggingFacility

5) Castle.Windsor

6) log4net

7) NUnit

8) Moq




## External sources:

For the file watching, some of the code is derived from 
[How to Use FileSystemWatcher Instead of Polling - Source Code](http://www.fascinatedwithsoftware.com/blog/post/2013/01/27/How-to-Use-FileSystemWatcher-Instead-of-Polling-Source-Code.aspx)


## Notes:
## 
The output sample xml has the ActualHeatRate section as shown below:
```
  <ActualHeatRates>
    <Name>Coal[1]</Name>
    <HeatRate>12.849293200</HeatRate>    
  </ActualHeatRates>  
```
  
 This was changed to the following so the xml can output more than one generators for that section:
```
   <ActualHeatRates>
    <Generator>
      <Name>Coal[1]</Name>
      <HeatRate>1</HeatRate>
    </Generator>
  </ActualHeatRates>
```
  
  
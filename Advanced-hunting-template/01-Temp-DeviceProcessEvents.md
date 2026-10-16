Kusto  

DeviceProcessEvents
| where Timestamp > ago(24h)
| project Timestamp, DeviceName, AccountName,
          FileName, ProcessCommandLine
| order by Timestamp desc
| take 100

--------------------------------------------

What each line means:  
DeviceProcessEvents  
Searches process execution events from endpoints.  

where Timestamp > ago(24h)  
Limits results to the last 24 hours.  

project  
Selects the columns you want to see.  

order by Timestamp desc  
Shows the newest events first.  

take 100  
Limits the output to 100 rows.  

This query is for investigation only. It does not modify devices or terminate processes.  

----------------------------------------------------------------

Investigate a suspicious process
When you find an interesting result, investigate:
- DeviceName: Which endpoint ran it?
- AccountName: Which account was involved?
- ProcessCommandLine: What command was executed?
- InitiatingProcessFileName: What launched the process?
- Timestamp: When did it happen?
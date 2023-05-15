### Description
In **FastSwitchboard.sol**, comments of the **"totalWatchers mapping"** says that the first parameter should be  **"dst chain slug"**, but in the **attest()** method, **"srcChainSlug_"** is being used. This explains that the **"Contract fails to deliver what was promised, but no one's security is affected"** . 

```
// dst chain slug => total watchers registered
    mapping(uint256 => uint256) public totalWatchers;
    
    if (attestations[packetId_] >= totalWatchers[srcChainSlug_])
```

### Expected behavior

dst chain slug should be used.

### Actual behavior

srcChainSlug has been used

### Screenshots

![Screenshot from 2023-05-15 14-21-49](https://github.com/UVvirus/SocketDL_bug_report/assets/39599249/8fbde88d-29b7-44b3-ad1c-7f80238db8c0)

![Screenshot from 2023-05-15 14-22-06](https://github.com/UVvirus/SocketDL_bug_report/assets/39599249/65669125-4f31-46bd-a40c-7d5045381b2c)


### Additional information

Severity: Low

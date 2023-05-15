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

If applicable, add screenshots to help explain your problem.

### Additional information

Severity: Low

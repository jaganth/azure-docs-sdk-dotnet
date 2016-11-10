---
uid: 
remarks: *content
---
## Remarks  
 The resize operation requests that the pool be resized.  The request puts the pool in the [Microsoft.Azure.Batch](assetId:///N:Microsoft.Azure.Batch?qualifyHint=False&autoUpgrade=True) allocation state.             The Batch service will perform the actual resize without any further client action, and set the allocation state to [Resizing](assetId:///T:Microsoft.Azure.Batch.Common.AllocationState?qualifyHint=False&autoUpgrade=True) once complete.  
  
 You can only resize a pool when its [AllocationState](assetId:///P:Microsoft.Azure.Batch.CloudPool.AllocationState?qualifyHint=False&autoUpgrade=True) is [Steady](assetId:///T:Microsoft.Azure.Batch.Common.AllocationState?qualifyHint=False&autoUpgrade=True).             You cannot resize pools which are configured for automatic scaling (that is, the [AutoScaleEnabled](assetId:///P:Microsoft.Azure.Batch.CloudPool.AutoScaleEnabled?qualifyHint=False&autoUpgrade=True) property of the pool is true).             If you decrease the pool size, the Batch service chooses which nodes to remove.  To remove specific nodes, call [RemoveFromPoolAsync](assetId:///M:Microsoft.Azure.Batch.CloudPool.RemoveFromPoolAsync(System.Collections.Generic.IEnumerable{System.String},System.Nullable{Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption},System.Nullable{System.TimeSpan},System.Collections.Generic.IEnumerable{Microsoft.Azure.Batch.BatchClientBehavior},System.Threading.CancellationToken)?qualifyHint=False&autoUpgrade=True).  
  
 The resize operation runs asynchronously.
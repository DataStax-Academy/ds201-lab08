<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">VNodes</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:academy@datastax.com">email</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
<span class="step-count"> Step 2 of 2</span>
   <a href='command:katapod.loadPage?[{"step":"finish"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Start the nodes in the cluster and examine the token distribution</div>


✅ Start *node1*
```
/workspace/ds201-lab08/node1/bin/cassandra
```
Wait for it to start

✅ Start *node2*
```
/workspace/ds201-lab08/node2/bin/cassandra
```
---
**Note:** You may be able to catch the log message describing the generated tokens as the nodes start up:
---


Use `nodetool` to verify that both nodes are running. (You may need to run this command multiple times.)

✅ Run `nodetool status`:
```
nodetool status
```
You should see that the Tokens column shows 128 tokens for each node.

<img src="https://katapod-file-store.s3.us-west-1.amazonaws.com/ds201/lab08-image02
.png" />

✅ Run `nodetool ring`  
```
nodetool ring
```
Notice how each node is responsible for smaller, but much more numerous sections of the token ring.

<img src="https://katapod-file-store.s3.us-west-1.amazonaws.com/ds201/lab08-image03.png" />

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
    <a href='command:katapod.loadPage?[{"step":"finish"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

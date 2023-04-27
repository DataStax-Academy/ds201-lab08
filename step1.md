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
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
   <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
<span class="step-count"> Step 1 of 2</span>
</div>

<!-- CONTENT -->

<div class="step-title">Edit <i>cassandra.yaml</i> to use <i>VNodes</i></div>

In this exercise there is a two-node Cassandra cluster. The root directories for the nodes are: `./node1` and `./node2`. You are going to edit the configuration file (`cassandra.yaml`) for *node2*. You are going to assign an `initial_token` value of `-9223372036854775808`


✅ Open `/workspace/ds201-lab08/node1/conf/cassandra.yaml` in a *nano* or the text editor of your choice.
```
nano /workspace/ds201-lab08/node1/conf/cassandra.yaml
```

* Make sure that `intial_token` is commented out:


* Set `num_tokens` to `128`
---
`num_tokens: 128`

`...`

`# initial_token:`

---

Save and exit the editor.

✅ Make the same changes to  `/workspace/ds201-lab08/node2/conf/cassandra.yaml` 

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
   <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

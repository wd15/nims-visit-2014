% Title
% Daniel Wheeler
% 2014-04-27

# {#overview .step data-scale=8}

   
# {#title .step data-y=-2500 data-scale=4}

<p class="title">Simulation Management Tools</p>

<p class="footer">
    Daniel Wheeler &bull;
    December 12, 2014
</p>


# {#automate .step data-y=200 data-x=-2400}

# {#automate .step data-y=200 data-x=-2400}

<br>
<p class="title"> Automate </p>

# About me {#aboutme .step data-y=200 data-x=-800}

<br>
scientific/academic code developer
<br>
<br>
develop scientific Python tools
<br>
<br>
run/manage simulations
<br>
<br>
interested in reproducible research, see <code class="twitter">@wd15dan</code>

# Interested in... {.step data-y=200 data-x=800}

<p class="small" style="font-size: 30px;">
<br>
logging simulations <br><br>
replicating simulations <br><br>
building upon existing simulations <br><br>
meta-data standards for simulations <br><br>
curating simulations <br><br>
integration tests for simulations<br><br>
</p>
<b>Automate with open source tools!</b>

# Scientific Development Process {.step data-y=200 data-x=2400}

<br>
<img class="center" src="images/workflow.png"></img>

# Core Issues {#orthogonal .step data-y=1500 data-x=-2400}

<br> workflow control
<br><br> version control
<br><br> <p style="color: red;"> event control </p>

# Version Control {.step data-y=1500 data-x=-800}

<img class="vc" src="images/stack-of-files.png"></img>
<br>
maintains history of code changes 
<br>
<br>
but not code usage
<br>
<br>
integrated into scientific code development

# Event Control {.step data-y=1500 data-x=800 }

<br>
provide a **unique ID (SHA checksum)** for every workflow execution
<br>
<br>
capture **metadata**, not data
<br>
<br>
**not** workflow control or version control
<br>
<br>
partial solution: **Sumatra**, a simulation management tool

# Client-Side Solution: Sumatra {.step data-x=2400 data-y=1500}

<br>
**doesn't change my workflow**
<br>
<br>
records the **metadata** (not the data): parameters, environment, data
location, time stamps, commit message, duration, data hash
<br>
<br>
generates **unique ID** for each simulation

# Demonstration {#easytouse1 .step data-x=-2400 data-y=2800}

<br>

~~~~{.console}
$ smt init smt-demo
$ smt configure --executable=python --main=script.py
$ # python script.py params.json
$ smt run --tag=demo --reason="create demo record" params.json wait=3
Record label for this run: '0c50797f1e3f'
No data produced.
Created Django record store using SQLite
~~~~

# Local Web Interface {#webinterface .step data-x=-800 data-y=2800}

<iframe width="100%" height="100%" src="http://127.0.0.1:8000/" frameborder="0" border="0"> </iframe>

# Server-Side Solution {.step data-x=800 data-y=2800}

<iframe width="70%" height="20%" style="position: relative; top: 50px; left: 100px;" src="http://127.0.0.1:5000/" frameborder="0" border="0"> </iframe>

<img class="center" style="max-width: 70%; left: -30px; top: 150px;" src="images/diag.png"></img>

<!-- <img class="center" style="max-width: 40%; left: 200px; top: 400px;" src="images/appengine.png"></img> -->
<!-- <img class="center" style="max-width: 80%; left: -300px; top: -190px;" src="images/sumatra.png"></img> -->
<!-- <img class="center" style="max-width: 40%; left: -200px; top: 100px;" src="images/sql-alchemy-logo1.jpg"></img> -->

# Thanks! {.step data-x=2400 data-y=2800}

<br>
slides: [wd15.github.io/nims-visit-2014](http://wd15.github.io/nims-visit-2014/)
<br>
<br>
sumatra demo: [github.com/wd15/smt-demo](https://github.com/wd15/smt-demo)

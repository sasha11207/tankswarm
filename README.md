<h3>You just found..</h3>
<h1>TANKSWARM</h1>
TANKSWARM is a complete platform for conducting and analyzing load tests on web services and apps.

<h1>Tools & Features</h1>
<ul>
  <li>Docker Swarm - Easy Setup</li>
  <li>Phantom - Fast Web Client</li>
  <li>Yandex Tank - Accurate Load Scheduler</li>
  <li>Elastic Search - Scalable Data Collection</li>
  <li>Grafana - Beautiful & Immediate Results Analysis</li> 
</ul>

<h1>Architecture</h1>
TANKSWARM consists of two Docker Service Stacks that are littered over a Docker Swarm:
<br/><br/>
<ol>
  <li><b>App:</b> consists of 3 docker containers - NGINX, Elastic Search and Grafana.  This service stack controls the browser based load testing console, the  Elastic Search Time Series database to collect test data and Grafana dashboards to chart test results.</li>
  <li><b>Tank:</b> consists of one docker container consisting of Yandex Tank, Logstash and Metric Beat.  This service stack executes the load tests, pushges results into Elastic search via Logstash and Metric Beat.</li>
</ol>

<img src="http://github.com/masterlau/tankswarm/blob/architecture.jpg"/>

<h1>Setup & Configuration</h1>
<h2>Docker Swarm Setup</h2>
<ol>
  <li><b>Compute Instances</b>: You can use VM's or Bare Metal Machines to create your Docker Swarm</li>
  <li><b>Network</b>: Ensure your nodes are on the same subnet</li>
  <li><b>Ports</b>: Open the following ports:
     <ul>
       <li>TCP port 2377 for cluster management communications</li>
       <li>TCP and UDP port 7946 for communication among nodes</li>
       <li>UDP port 4789 for overlay network traffic</li>
    </ul>
  </li>
  <li><b>Operating System</b>: Ubuntu Xenial (16.04)</li>
  <li><b>Install Docker</b>
      <ol>
        <li></li>
    </ol>
  </li>
</ol>

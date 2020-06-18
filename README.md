The idea of this project was to try to get the demo: 

https://www.freertos.org/FreeRTOS-Plus/WolfSSL/FreeRTOS_WolfSSL_Example.html

working except with DSA encryption as opposed to RSA. There is a FCC requirement mandating that DSA encryption be used on the satellite
to ensure that the satellite is receiving commands from us as opposed to someone else. 

In this repoistory there currently are two branches. The dev branch contains a working version of the demo (using RSA encryption), and the dev_wip branch contains a
work-in-progress attempt to use DSA with the demo as opposed to RSA. I reached out to WolfSSL through their forum about the issue I was having but have
not yet gotten a response. 

These are Microsoft Visual Studio 2010 projects. 

Possible future areas of work:
<li>
  <ul>Convert the Microsoft Visual Studio 2010 projects into CMake projects</ul>
  <ul>Fix the dev_wip branch: Error -148 returned from CyaSSL_CTX_load_verify_locations() issue</ul>
  <ul>Succesfully send encrypted messages using DSA between the i.MXRT1050 and a laptop computer.  </ul>
  <ul>Create a custom protocol in Cosmos (https://cosmosrb.com/) that sends data using SSL</ul>
  <ul>Create a design document specifing the memory layout of the OBC (we want to store SSL certificate in persistent memory)</ul>
  <ul>Store the client SSL certificate in a secure location in the ground station? </ul>
</li>

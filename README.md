# NDNSim

Put these files in your scratch folder and execute the command from your ns-3 directory "./waf --run scratch/filename"
  
  All the files provided in the "examples/turtorial" is IP based.There are examples of NDN based programs ut some of them has some errors. So I made the modification and here are all the NDN based debugged working programs.
  
  Reference link:https://ndnsim.net/current/examples.html
  
All the files produces .xml files which can be further used with NetAnim for visualisation. The xml files are provided in the NetAnim Folder which can directly be used for visualisation.


v2i is for vehicle to interface. It requires the file "x-topo.txt".Put it in any directory and then add the location in the 92 of the v2i file.
v2v is for the vehicle to vehicle interface.



Both of the above files' original code gave the following error which has been taken care of:

"../scratch/v2i.cc: In function ‘int ns3::main(int, char**)’:
../scratch/v2i.cc:151:5: error: ‘NqosWifiMacHelper’ was not declared in this scope
     NqosWifiMacHelper wifiMacHelper = NqosWifiMacHelper::Default ();
     ^~~~~~~~~~~~~~~~~
../scratch/v2i.cc:151:5: note: suggested alternative: ‘WifiMacHelper’
     NqosWifiMacHelper wifiMacHelper = NqosWifiMacHelper::Default ();
     ^~~~~~~~~~~~~~~~~
     WifiMacHelper
../scratch/v2i.cc:153:5: error: ‘wifiMacHelper’ was not declared in this scope
     wifiMacHelper.SetType ("ns3::StaWifiMac", "Ssid", SsidValue (ssid),
     ^~~~~~~~~~~~~
../scratch/v2i.cc:153:5: note: suggested alternative: ‘WifiMacHelper’
     wifiMacHelper.SetType ("ns3::StaWifiMac", "Ssid", SsidValue (ssid),
     ^~~~~~~~~~~~~
     WifiMacHelper
../scratch/v2i.cc:165:23: error: expected ‘;’ before ‘wifiMac’
     NqosWifiMacHelper wifiMac = NqosWifiMacHelper::Default ();
                       ^~~~~~~
../scratch/v2i.cc:166:5: error: ‘wifiMac’ was not declared in this scope
     wifiMac.SetType ("ns3::ApWifiMac", "Ssid", SsidValue (ssid),
     ^~~~~~~
../scratch/v2i.cc:166:5: note: suggested alternative: ‘WifiMac’
     wifiMac.SetType ("ns3::ApWifiMac", "Ssid", SsidValue (ssid),
     ^~~~~~~
     WifiMac
"


# Video and Presentation Slides

Please find below a link to a video presenting the approach and the corresponding slides showing how the ridesharing plans have been computed.

<a href="http://ucc.insight-centre.org/varmant/presentationDemoSlides/videoSpeech.mov"> Video </a>

<a href="http://ucc.insight-centre.org/varmant/presentationDemoSlides/presentationDemo18.pdf"> Slides </a>

# Demo: Interactive solution of a ridesharing problem

Find in the links below a demo simulating a system wide ridesharing plan through an interactive solution.  These scenarios show two drivers sharing their journeys with three riders. The first link illustrates a ridesharing plan aiming at maximizing the number of users. The second link shows a ridesharing solution  aiming at maximizing the number of passengers.
In the demo, the three rider requests arriving at the same time are collected before a system wide plan is computed, (click "next request"). To visualize the ridesharing plan click on the button "compute plan". To visualize an execution of the ridesharing plan click "show plan". Moreover, all movable objects, i.e., cars and riders, are clickable and display the current information about their state.
	

<a href="http://ucc.insight-centre.org/varmant/scenarioDemo/demoMaxUsers_start.html"> Demo Maximising the number of users (drivers and passengers) </a>


<a href="http://ucc.insight-centre.org/varmant/scenarioDemo/demoMaxPassengers_start.html"> Demo Maximizing the number of passengers </a>


# ridesharing_pb_instances

The repository contains a set of ridesharing instances for three ridesharing clusters in Norway, Texas, California.

Norway

<a href="http://ucc.insight-centre.org/varmant/rsp_instances/Norway_noShifters_dayId1_nbMonths24.tar.gz"> Norway dataset with no shifters  </a>

<a href="http://ucc.insight-centre.org/varmant/rsp_instances/Norway_withShifters_dayId1_nbMonths24.tar.gz"> Norway dataset with shifters </a>

Texas

<a href="http://ucc.insight-centre.org/varmant/rsp_instances/Texas_noShifters_dayId1_nbMonths9.tar.gz"> Texas dataset with no shifters </a>

<a href="http://ucc.insight-centre.org/varmant/rsp_instances/Texas_withShifters_dayId1_nbMonths9.tar.gz"> Texas dataset with shifters </a>

California

<a href="http://ucc.insight-centre.org/varmant/rsp_instances/California_noShifters_dayId1_nbMonths9.tar.gz"> Norway dataset with no shifters </a>

<a href="http://ucc.insight-centre.org/varmant/rsp_instances/California_withShifters_dayId1_nbMonths9.tar.gz"> Norway dataset with shifters</a>



# Acknowledgment

These Ridsharing problem instances have been built from a dataset of advertised trips that were provided by Carma Technology Limited (http://www.gocarma.com/)

# Ridesharing Problem Instance Description

Each file in the dataset is described as follow:

The Comments start with #  
The character '\t' is used as a separator between labels and values  
Meaningfull lines have the following form:  
     label:'\t'value or 
     label:'\t'value1'\t'...'\t'\tvalueN 

Drivers, Riders and Shifters (i.e. drivers willing to become passengers) are described as follow:

Drivers 

 driver:  String                         the driver's label
  dId:  int                              the driver's local id within the driver set 
  uId:  int                              the driver's global id wintin the user set
  starts_from:  int                      the driver's start node 
  ends_to:  int                          the driver's end node 
  starts_after:  int                     the driver's earliest sart time (in secondes)
  ends_before:  int                      the driver's latest arrival time (in secondes)
  fastest_path_time:  int                the driver's fastest path duration (in secondes)
  feasible_match_rIds:  int ... int      the driver's list of feasible rider matches i.e potential passenger 
  path_of_nodes:  int ... int            the driver's path nodes from start to end  
  min_time_to_nodes:  int ... int        min_time_to_nodes[i] is the travel duration (in secondes) for the driver to reach node path_of_nodes[i]  
  min_dist_to_nodes:  dble ... dble      min_dist_to_nodes[i] is the travel distance (in kms) for the driver to reach node path_of_nodes[i]  

 		... more drivers ...


 Riders
 
 rider:  String                          the rider's label 
  rId:  int                              the rider's local id  within the rider set 
  uId:  int                              the rider's global id  within the user set
  starts_from:  int                      the rider's start node 
  ends_to:  int                          the rider's end node 
  starts_after:  int                     the rider's  earliest sart time (in secondes)
  ends_before:  int                      the rider's latest arrival time (in secondes)
  fastest_path_time:  int                the rider's fastest path time duration (in secondes)
  feasible_match_dIds:  int ... int      the rider's list of feasible driver matchs 
  match_dId:  int                       the contextual driver match  
  pick_up_path:  int ... int           the rider's pick-up path to meet the contextual match_dId  
  pick_up_path_dist:  int              the rider's pick-up path distance (in Kms) to meet the contextual match_dId  
  drop_off_path:  int ... int          the rider's drop-off path to meet the contextual match_dId  
  drop_off_path_dist:  int             the rider's drop-off path distance (in Kms) to meet the contextual match_dId  

		... more riders ...


 Shifters dId:rId 

int:int	... int:int    					lits of mapping rId:dId corresponding each to one shifter 







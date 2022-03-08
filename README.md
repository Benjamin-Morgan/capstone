USERS    -	required? -	type	-  description
username	     y	      str	     PRIMARY KEY
first_name	   y	      str	
last_name	     y	      str	
gender	       y	      str	
password	     y	      srt	     min 6 char long
dob            y	      date	   YYYY-MM-DD format
email        	 y	      str	     must be valid
country	       y	      str	     must use IOC
weight	       n	      int	
max_heart_rate n	      int	
email_permission n	    bool	
			
			
WORKOUT			
type	         y	      str	      must be one of: rower, skierg, bikem slides, water
date	         y	      date	    YYYY-MM-DD format
timezone	     n	      str	      valid timezone format from the tz database
distance	     y	      int	      Meters
time 	         y	      int	      In tenths of seceond, one minute = 600
weight_class	 depends	str	      required if type is rower, dynamicm or slides. H or L
verified	     optional	bool	
comments	     n	      str	
workout_type	 n	      str     	must be one of: check docs
stroke_rate	   n	      int	      avg stroke rate
heart_rate	   n	      obj	      obj of str following optinal values: avg, min, max, end, recovery
stroke_count	 n	      int	      total #
calories_total n	      int	      total #
drag_factor	   n	      int	      avg drag factor
rest_distance	 depends	int	      for interval workouts only
rest_time	     depends	int	      for intervals
workout 	     n	      array	    array of objects containing split or intercal data, see below
stroke_data	   n	      array	    array of objects containing stroke data see below
metadata	     n	      obj	
			
			
workout details			
splits	       n	      array	
intervals	     n	      array	
targetrs	     n	      obj	
			
Stroke Data			
t	             n	      int	      Time in tenths of second eg 23 is 2.3 seceonds
d	             n	      int	      Distance, in decimeters eg 155 is 15.5 meters
p 	           n	      int	      Pace in tenths of seceonds eh 971 is 1:37.1
spm	           n	      int	      strokes per minute
hr	           n	      int	      heart rate

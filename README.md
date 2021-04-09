# Cloud
Cloud Data- CSV
Source of data:

Philippe Collard -  California Space Institute 
		    A-021, UCSD
		    La Jolla, CA 92093
		   (619)534-6369
		   27799::collard  (decnet)

;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;

;                   CLOUD DATABASE
;The data sets we propose to analyse are constituted of 1024 vectors, each
;vector includes 10 parameters. You can think of it as a 1024*10 matrix.
;To produce these vectors, we proceed as follows:
;
;	- we start with two 512*512 AVHRR images 
;	  (1 in the visible, 1 in the IR)
;	- each images is divided in super-pixels 16*16 and in each
;	  super-pixel we compute a set of parameters.
;
;		visible: mean, max, min, mean distribution, contrast,
;			 entropy, second angular momentum
;		IR: mean, max, min

;The set of 10 parameters we picked to form the vectors is a compromised between
;various constraints. Actually we are still working on the choice of parameters
;for the data vectors. The data set I send you has not been normalized. The
;normalization of the data set is required by our classification scheme but that
;may not be true for yours. To normalize the data we compute the mean and
;standard deviation for each parameter on the entire data set then for each
;parameter of each vector we compute: 
;
;	Norm. value = (un-norm value - mean)/SD	where
;
;	mean = mean value for this particular parameter over the data set
;	SD   = standard deviation .....
;

A package to allow the Invisible Higgs samples to decay with Pythia.

Assuming Pythia can be run with the already exisiting object file: pythia-6.4.28.o
If not make sure your gfortran location is in your path:

$ which gfortran
$ gf=$(which gfortran)
$ export PATH=$gf:$PATH

or put in your bash profile for convenience

then:

$ gfortran -c pythia-6.4.28.f



Start by running the script:

      ./decayLHEs

    This should compile the analysis code main81.f with Pythia.

Note, this needs to be run each time the code changes.

Then run the executable:

     ./decay

This allows the hard process to decay through Pythia.

NB:
	main81.f is a generic code that reads an LHE, made either externally or with Pythia,  and allows analyses of the process contained
NB:
	LHEinfo.sh is a script that returns the number of events stored per lhe. It requires the LHE as an argument.
NB:	
	The Higgs decay H-> Z Z is known to Pythia with the decay mode number: 225
	The Z decay Z -> v v is known to Pythia with the decay mode number:  183/ 185/ 187 for electrons, muon & tau neutrinos

	The PDG ID for the Higgs= 25
          	    	 Z boson= 23
		      e neutrino= 12
	             mu neutrino= 14
	            tau neutrino= 16

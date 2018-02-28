# Program-1.11
Intro to Java Programming, Comprehensive Version, 10th Edition, Y. Daniel Liang

Question:

         (Population projection) The U.S. Census Bureau projects population based on the 
         following assumptions: 
         ■ One birth every 7 seconds 
         ■ One death every 13 seconds 
         ■ One new immigrant every 45 seconds  
         Write a program to display the population for each of the next five years. 
         Assume the current population is 312,032,486 and one year has 365 days. 
         
Code:

        public class s_1_11 {

           public static void main (String args[]){
          
          //rates are in seconds
          double birthRate = 7.0; 
          double deathRate = 13.0; 
          double newImmigrant = 45.0;

          double currentPop = 312032486;

          double secondsInYear = 60 * 60 * 24 * 365;

          double numBirths = secondsInYear / birthRate;
          double numDeaths = secondsInYear / deathRate;
          double numImmigrants = secondsInYear / newImmigrant;
           
          //counting the next 5 years
          for(int i = 1; i <=5; i++){

            currentPop += numBirths + numImmigrants - numDeaths;
            System.out.println("Year " + i + " = " + (int)currentPop);
	    }
	  }
	}

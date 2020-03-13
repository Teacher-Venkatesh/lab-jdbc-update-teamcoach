![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Lab | ProGrad Premier League


## Progression 1:

1. Create a class called as `Team` with below attributes, 
```
	- teamName - String 
	- coachName - String 
```
2. Include getter and setter method for all the attributes 
3. Include a constructor with below arguments, 
 	- `public Team(teamld,teamName,coachName) `



## Progression 2:

1. Create a dao-class called as `TeamDAO` with below methods, 
	- `public List<Team> getAllTeams()` - Method used to get all the users from the database 
	- `public void updateTeamDetails(String teamName,String coachName)` - Method used to update the team's coach details (coach name) 
	- `public static void displayTeams(List<Team> teamList)` - Method used to display the team coach details 
2. In DAO classes set the database connection.  

## Progression 3:
1. Create a class called as `Main`.
2. Create appropriate objects and call the methods to display the details.
3. Refer sample input and output for reference.


![1 2](https://user-images.githubusercontent.com/61002120/76416050-5807d380-63c0-11ea-8d52-9e8750e800f9.png)


### Note:

Use the below code to retreive the connection details from jdbc.properties to establish connection
```
public static Properties loadPropertiesFile() throws Exception {
	Properties prop = new Properties();	
	InputStream in = ConnectionManager.class.getClassLoader().getResourceAsStream("jdbc.properties");
	prop.load(in);
	in.close(); 
	return prop;
}
```    
**Sample Input and Output**
```
Team List Name 		Coach 
India		 	Paddy Upton 
Australia 		Brad Hodge 
England			Sanjay Bangar 
South Africa		Ricky Ponting 
America			Supergiants Stephen 
Enter the teamname you want update 
India 
Enter the new coachname you want update 
Anil Kumble 
Updated team list 
Name 			Coach
India		 	Anil Kumble
Australia 		Brad Hodge 
England			Sanjay Bangar 
South Africa		Ricky Ponting 
America			Supergiants Stephen 
```

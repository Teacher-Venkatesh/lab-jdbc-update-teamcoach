![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Lab | ProGrad Premier League


## Progression 1:

Create `Main.java` with main method 
Create `Team.java` domain class with below attributes, 
```
teamName - String 
coachName - String 
```
Include getter and setter method for all the attributes 
Include a constructor with below arguments, 
`public Team(teamld,teamName,coachName) `



## Progression 2:

Create `TeamDAO.java` with below methods, 
`public List<Team> getAllTeams()` - Method used to get all the users from the database 
`public void updateTeamDetails(String teamName,String coachName)` - Method used to update the team's coach details (coach name) 
`public static void displayTeams(List<Team> teamList)` - Method used to display the team coach details 
In DAO classes set the database connection.  


![1 2](https://user-images.githubusercontent.com/61002120/76416050-5807d380-63c0-11ea-8d52-9e8750e800f9.png)


### Note:

Use the below code to retreive the connection details from mysql.properties to establish connection
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

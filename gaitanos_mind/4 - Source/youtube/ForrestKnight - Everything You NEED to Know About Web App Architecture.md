12:42 Tue 7th January 2025

Tags: #youtube #webdevelopment 

---
https://youtu.be/sDlCSIDwpDs?si=zN2LjQqTRwxwlqjs

Web app architecture - the blueprint of how the webapp is structured.
What app do you want to build?
How many tiers is your application?
	![[Pasted image 20241221103608.png]]

***SPONSOR-Jet-brains space***

1. **Client-server architecture**
	![[Pasted image 20241221105139.png]]
	1. Tier 1 ![[Pasted image 20241221105605.png]]
	2. Tier 2![[Pasted image 20241221105827.png]] ![[Pasted image 20241221105952.png]]
	4. Tier 3![[Pasted image 20241221110532.png]]
	Takes into account the single responsibility principle.
	
2. **Peer-to-peer architecture**
	![[Pasted image 20241221111339.png]]
	Don't need a central server. Rules out possibility of single point failure.
	
3. Monolithic Architecture
		![[Pasted image 20241221112418.png]]
		It's not scalable.
		When changes are made to the code, you are required to deploy the entire application, again.
		Bugs in the code break the whole application.
		
4. Microservice Architecture
		![[Pasted image 20241221103527.png]]
		It's modular
		Collection of services that each serve a unique responsibility.
		Each service can be scaled independently.
		
5. Serverless Architecture
		![[Pasted image 20241221112317.png]]
		Also known as serverless computing.
		A function or a service (which is a part of the microservice responsibility) is hosted by a third party.

### See also:

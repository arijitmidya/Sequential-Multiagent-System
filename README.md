# Sequential-Multiagent-System

Sequential Process Overview
The sequential process ensures tasks are executed one after the other, following a linear progression. This approach is ideal for projects requiring tasks to be completed in a specific order.

Key Features
Linear Task Flow: Ensures orderly progression by handling tasks in a predetermined sequence.
Simplicity: Best suited for projects with clear, step-by-step tasks.
Easy Monitoring: Facilitates easy tracking of task completion and project progress.

Advanced Features
​
Task Delegation
In sequential processes, if an agent has allow_delegation set to True, they can delegate tasks to other agents in the crew. This feature is automatically set up when there are multiple agents in the crew.

Asynchronous Execution
Tasks can be executed asynchronously, allowing for parallel processing when appropriate. To create an asynchronous task, set async_execution=True when defining the task.

Memory and Caching
CrewAI supports both memory and caching features:

Memory: Enable by setting memory=True when creating the Crew. This allows agents to retain information across tasks.
Caching: By default, caching is enabled. Set cache=False to disable it.

Implementation : 

![image](https://github.com/user-attachments/assets/1a36594c-294a-4667-8c55-5ee31828ced6)


The crew comprises of :
1. Agents : 2 (venue_finder , venue_quality_assurance_agent )
2. Tasks : 2 (find_venue_task , quality_assurance_review_task )
3. Tools : 1 (SerperDevTool)
4. Crew = Goal + Agents + Tasks + Tools 

Hyperparameters to play with : 

Agents : 
  max_iter=15,  # Optional
  max_rpm=None, # Optional
  max_execution_time=None, # Optional
  verbose=True,  # Optional
  allow_delegation=False,  # Optional


Steps to execute the project in VS code .

Step 1 : Download all the files 

Step 2 : Create a project and upload the files

Step 3 : run the requirements.txt file ( command : pip install -r requirements.txt ) . The application is build on python==3.12

Step 4 : update the .env file with the values : 

OPENAI_MODEL_NAME='gpt-4o-mini'
OPENAI_API_KEY='add your key'
SERPER_API_KEY='add your key'

Link to get the  keys : https://serper.dev  &   https://platform.openai.com/

Step 5 : Define the research topic 

# Define the input for the event planning crew 
    inputs = {
        "conference_name": "AI Innovations Summit",
        "requirements": "Capacity for 5000, central location, modern amenities, budget up to $50,000"
    }

Step 6 : Run the main.py file ( command : python main.py ) and you will see the magic in the console 


Sample output : i am not highlighting the execution process , chain of thought , delegation and all , only highlighting the final output 

### Detailed Review of Top 5 Conference Venues

1. **The Ritz-Carlton, Atlanta**
   - **Location:** Downtown Atlanta, Georgia
   - **Capacity:** Up to 1,000 guests
   - **Amenities:** High-speed internet, audio/visual support, on-site catering, luxury accommodations, business center.
   - **Pricing:** Starting at $200 per person for full-day packages.
   - **Availability:** Open year-round, various booking options.
   - **Overview:** This venue is highly regarded for its elegance and upscale service, making it ideal for high-profile corporate events. The amenities are comprehensive and designed to cater to the needs of executives. Potential issues include the higher pricing point, which may not be suitable for all clients, but the luxury accommodations and service quality generally justify the cost.

2. **Marriott Marquis San Diego Marina**
   - **Location:** San Diego, California
   - **Capacity:** Over 100,000 square feet of event space
   - **Amenities:** Ocean views, poolside venues, multiple breakout rooms, full-service catering, on-site technology services.
   - **Pricing:** Custom pricing depending on event details.
   - **Availability:** Early booking recommended due to high demand.
   - **Overview:** This venue offers a majestic backdrop with its ocean views, making it perfect for large conferences. It provides flexibility with multiple spaces to suit varying event needs. A potential drawback is the custom pricing, which may lead to higher costs depending on the specifics of the event, but the amenities and location are significant draws for attendees.

3. **Hyatt Regency Chicago**
   - **Location:** Chicago, Illinois
   - **Capacity:** Over 2,000 guests
   - **Amenities:** Modern conference rooms, rooftop space, multiple dining options, in-house event planning.
   - **Pricing:** Conference packages starting at $175 per person.
   - **Availability:** Available year-round; booking varies by demand.
   - **Overview:** As one of the largest venues, it combines capacity with modern amenities, making it suitable for large-scale events. The in-house event planning adds convenience, though the size may lead to feelings of being impersonal. The competitive pricing compared to similar venues makes it a strong contender; however, it's essential to ensure enough staff availability for targeted service.

4. **The Peabody Memphis**
   - **Location:** Memphis, Tennessee
   - **Capacity:** Up to 1,500 guests
   - **Amenities:** Unique duck march, extensive audiovisual capabilities, on-site spa, and dining.
   - **Pricing:** Event packages starting at $150 per person.
   - **Availability:** Historic venue; early reservations advised.

5. **Sheraton Grand Sydney Hyde Park**
   - **Location:** Sydney, Australia
   - **Capacity:** Up to 1,200 guests
   - **Amenities:** Stunning park views, outdoor terrace, business facilities, full catering support, on-site accommodations.
   - **Pricing:** Starting packages from AUD $160 per person.
   - **Availability:** Popular for international events; advanced booking required.
   - **Overview:** This venue combines gorgeous scenery with practicality, making it an excellent choice for international meetings. The outdoor terrace and park views are unique selling points. However, its high popularity may lead to limited availability, necessitating early planning. Given its features and pricing, it remains attractive for hosting prestigious events seeking a beautiful setting.

### Conclusion
These five venues have been analyzed based on capacity, amenities, pricing, and overall suitability for conference events. Each venue offers distinct benefits and potential hurdles, catering to different client needs and event types. When selecting a venue, factors such as budget, event size, and specific requirements should guide your choice to ensure an optimal experience. It's advisable to contact these venues for the most current information and to secure bookings in advance to meet the desired requirements.












  
  
  

# ai-social-good-project
This is an AI system to help manage food waste issues.

##Problem

I decided to focus on the issue of food waste which relates to topic 12 of the UN SDG’s, responsible consumption and production. It also connects to topic 2 which is zero hunger. It affects the group of people that struggles to pay for their food consumption, such as homeless people, low-income households and college students, as more knowledge about the issue and a better network could form connections that minimize waste and improve people with hunger all at once.
I believe that the topic is missing certain regulations, such as strict rules for restaurants or grocery stores. Additionally, better education about different labels, for example “best by” or “sell by” could improve the situation in private households. The correct discarding of trash is also important, so people need to choose the right trash cans. This issue is severe in the U.S. in general, since SanJoséRecycles.org reports that 40% of food is wasted. Waste management is often addressed by San Jose officials and in severe need of improvement. 

##AI Capability

The AI capability I used in this lab is natural language processing for structured data extraction. The system gets unstructured text, in this case either a complaint or a question, and sorts it into structured fields determined by a schema such as location, waste type, urgency, responsible department and entity type.

This fits well because the main failure point is unstructured input either in the form of a text description or a picture. NLP then takes that input and converts it into a reliable pattern that will not change evaluation either if the code is run several times in a row. This ensures reliable decision-making and consistency for similar inquiries.

##Workflow

*   Input: Either complaint or question. E.g., someone could upload a picture of a dumpster behind a restaurant to file a claim of improper waste management. Another person could upload a picture or describe a food item with a specific date label and ask about the edibility of this product and how much grace period there is after the date.

*   AI Process: The AI would either evaluate the picture in terms of edibility/amount/kind of items in order to determine the type of  complaint and then start an official complaint process, asking for details to determine if a business or private household is accused. The complaint will then be forwarded to the specific department. The final evaluation if the complaint is valid will be done by humans of a specific department.
Otherwise the AI will answer the question by analyzing if it is about waste disposal/expiration date/giving away food. For the examples above, AI would forward an official complaint for case one and answer the expiration date question by giving a specific time estimate for example two.

*   Output: AI will output a summary of the reported complaint and contact details for the specific department or it will provide an answer specialized for each food item and clearly state where to dispose it, when to eat it or where to give it as you can see in the attached images of output.

<img width="2880" height="1626" alt="Image 5-9-26 at 7 07 PM" src="https://github.com/user-attachments/assets/e589c6f3-5708-498b-8cd6-0f8d3442a40b" />
<img width="2880" height="1626" alt="Image 5-9-26 at 7 06 PM" src="https://github.com/user-attachments/assets/2cfd5f1e-7c72-47fa-a51f-11c6f8885f68" />


*   Real-World Action: Regulations will be enforced strictly following the complaint and people asking questions can implement the newly gained knowledge in their behavior and habits to minimize waste and tackle hunger at the same time. (maybe business would learn about apps like "Too Good To Go" to eliminate unnecessary waste).

##Failure Case

I asked AI to help me build the framework to input an edge case prompt because I was not sure how to input it without changing my prior code. I then changed the prompt to my own made-up one where the entity type was unknown. In this case the accused_entity_type is unknown and therefore a somewhat unoffical complaint would not lead to proper results. This is a near-miss because the evaluation is correct, there is just important information missing that the AI would have needed to request clarification.

<img width="2602" height="1122" alt="Image 5-9-26 at 7 11 PM" src="https://github.com/user-attachments/assets/6ddad79d-65fb-46b3-ba96-67c5e87a8ea6" />


##Oversight and Tradeoff

Human review sits right after AI provides the structured output. Humans will be the ones verifying the complaints and taking action in consequence to them. If a complaint has null values or fields that are unknown, it is the human's job to fill in or even find out the missing data in serious cases. Vague descriptions can be a cause for the need of human check ups. This can make the process less efficient, but having knowledge and accuracy about illegal food waste is of higher importance. Therefore, in some cases there will be a trade-off in efficiency due to missing data because decisions need accountability.



# ethicalbankingrecommender
#Pulls transaction data using Capital One API and recommends ethical buying options.

#Features:
#*Identifies alternative options based on shopping transaction history using open-web Corporate Social Responsibility company ratings.
#*Makes one recommendation at a time so as not to flood the customer.
#*Allows opt out of the recommender service.
#*Allows option to see a detailed responsibility assessment of a company.

#Platforms used:
#*Microsoft Flow
#*Twilio
#*Sharepoint (lookup library/simulated DB)

#Summary of operation:
#*SMS sent to customer saying they have signed up for ethical buying recommendations and asking if they'd like one.
#*Transaction history is preloaded for better performance. (For the purpose of the simulation, random customer data is generated).
#*If buyer indicates yes, the program lists transactions from the last 30 days in descending order of value. Using the top 10 (a performance consideration), it refers to the database for alternative options.
#*One recommendation at a time is provided, including a tinyurl linking to a more detailed responsibility assessment for the company. 
#*Customer is asked if they'd like another recommendation.
#*If customer replies No to ethical buying recommendations, they are given options to unsubscribe.

#Assumptions: [i]Customer has appropriately consented to opt in to the service and be contacted about it. [ii]Transaction data from the API yields merchant ID. [iii]Lookup of merchant ID to responsibility credentials. [iv] Merchant ID exists in the responsibility lookup.

#Notes: [a] artifical merchant ID is appended to transaction records as this is not currently available in the C1 API. [b] a small generic dataset for recommender options is provided, this is not a full recommender system for the purpose of the proof of concept. With a full dataset, a fully featured recommender platform could be introduced using a range of datasets relating to ethical buying options, customer ratings on ethical dimensions, and potentially other customer attributes (for example age) to tailor recommendations to customers. [c] For production, the completeness of the mercharnt ID to responsibility credentials lookup would be key and this would need assurance to e.g. avoid confusion of similar company names, track changes in company names. [d] Terms and conditions of service for this app would be important, including to make it clear that no specific endorsement is provided, where the recommendation data comes from, and to make it clear that this is external data which C1 is using and no company has paid to promote their service. 

#Further development options: [I] The trigger condition could be made part of the service, for example customer can choose whether ethical buying suggestions are provided annually, monthly, weekly, or for particular company category types (for example retail, cosmetics, insurance). [II] Customers could be given the option to tailor their preferences for responsibility aspects and use the detailed CSRHub API to upweight alternative buying options based on the various detailed indices held by CSRhub e.g. equality/gender diversity, environmental.

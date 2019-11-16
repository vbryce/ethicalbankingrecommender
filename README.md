# ethicalbankingrecommender
#Pulls transaction data using Capital One API and recommends ethical buying options.

#Features:
#1)Identifies alternative options based on shopping transaction history using open-web Corporate Social Responsibility company ratings.
#2)Makes one recommendation at a time so as not to flood the customer.
#3)Allows opt out of the recommender service.
#4)Allows option to see a detailed responsibility assessment of a company.

#Platforms used:
#-Microsoft Flow
#-Twilio
#-Sharepoint (lookup library/simulated DB)

#Assumptions: [i]Customer has appropriately consented to opt in to the service and be contacted about it. [ii]Transaction data from the API yields merchant ID. [iii]Lookup of merchant ID to responsibility credentials. [iv] Merchant ID exists in the responsibility lookup.

#Notes: [a] artifical merchant ID appended to transaction records as this is not currently available in the C1 API. [b] a small generic dataset for recommender options is provided, this is not a full recommender system for the purpose of the proof of concept. With a full dataset, a fully featured recommender platform could be introduced using a range of datasets relating to ethical buying options, customer ratings on ethical dimensions, and potentially other customer attributes (for example age) to tailor recommendations to customers. [c] For production, the completeness of the mercharnt ID to responsibility credentials lookup would be key and this would need assurance to e.g. avoid confusion of similar company names, track changes in company names. [d] Terms and conditions of service for this app would be important, including to make it clear that no specific endorsement is provided, where the recommendation data comes from, and to make it clear that this is external data which C1 is using.

## Veteran Identification Card (VIC)


## Sprint 0

### Problem Statement
There are a variety of situations in which Veterans need to prove their Veteran status in order to receive a particular benefit (having [a way to prove Veteran status](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/profile/military-information/discovery-and-research/2023-military-info-discovery/findings-summary.md#though-they-may-not-need-their-dd214-in-all-cases-to-apply-for-va-benefits-having-a-copy-of-it-facilitates-the-benefit-application-process-and-helps-veterans-access-non-va-privileges-memberships-and-discounts) helps Veterans access non-VA privileges, memberships, and discounts). Veterans would benefit from an easy-to-access official Veteran ID card to use in these contexts. Because there is currently no simple way to attain an ID like this, a widely accepted Veteran ID within the mobile app could prove a very useful feature for Veterans and greatly increase usage of the app.

From VA.gov: 
>“A Veteran ID Card (VIC) is a digital photo ID you can use to get discounts for Veterans at many stores, businesses, and restaurants. When you have this card, you won’t need to carry around your military discharge papers or share sensitive personal information to get discounts. And you don’t need to request another type of photo ID card to prove you’re a Veteran or to get retail or business discounts.”
*Veterans must have an honorable discharge to get the ID*

### Current Experience
#### In app:
While VIC card is not currently present in the VA Mobile app, Veterans occasionally report using letters in the VA Letters section of the VA mobile app as proof of service. 

#### Outside the app:
Currently,the processes for acquiring a VIC card are cumbersome and long and not well known by Veterans. 

**Getting a VIC**(From [How To Apply For A Veteran ID Card](https://www.va.gov/records/get-veteran-id-cards/vic/)):
- Step 1: Veteran applies for VIC card (requires doing the following: Fill out form (digital or paper), upload or print a photo to attach to form. Requires SSN, a digital copy of their DD214, DD256, DD257, or NGB22, a copy of a current and valid government-issued ID.
- Step 2: Application is received, reviewed and the photo must be approved (exactly how long does this take?)
- Step 3: Veteran receives an email letting them know status of application. They may be asked for additional info or evidence.
- Step 4: If eligible, Veteran receives digital VIC card (pdf) in an email.
- Step 5: Veteran must print the digital VIC card (pdf) in order to use it (this cost is covered by the Veteran).

**Using a VIC:**
- Veteran needs to remember to have VIC card with them when it's needed to prove Veteran status.


### Notes:
* VIC =  Veteran identification card (Veterans love it)
  * Identify themselves as a veteran at businesses
  * Intended to be printed
  * Must include a photo
       * Uploading/approving/printing a photo is the key part of this
       * **This is something to investigate if we can do a photo-less version**
  * Super expensive, single point of failure
  * Can be digital now
       * Emailed to you
  * Possible approaches
       * Ignore the photo requirement and automate it in the app, like letters
       * Perfect for a mobile app
       * Consider as part of apple wallet
* We don’t want to replace the VIC, but want something that can serve the same purpose in the app.
* Process for applying is long and opaque.  Long process and then you get a PDF to be printed.  Previously sent to Office Depot to be printed but that was too expensive
  * Email from VA has 2 PDFs, one of the front of the card and one of the back.
  * The VIC law is prescriptive and doesn’t include funding so Veterans need to pay to print the card which is not worth it.
  * The photo is the hardest part, needs to be approved and holds up the process.  The photo is part of the law.  We may be able to bypass that if we do something that isn’t technically the VIC but serves the same purpose but could be automated.
  * There is an ID # on the card

### Pain Points
* Acquiring a VIC is time consuming
* Veterans need to pay to print the card
* Veterans need to remember to have VIC (or some other form of accepted Veteran ID) with them to receive benefits

### Assumptions and Level of Confidence
TBD


### Risks
1. Creating a ‘competitor’ to the VIC could anger certain stakeholders (?) 
    1. Need to ensure creating an ID card that is not technically the VIC does not interfere with the VIC law
2. Surfacing current VIC may not be technically possible and the owning group may not have interest in working with us
3. If we aren't able to let the 3rd parties who currently accept VIC as a form of proof of Veteran status know that the digital VIC is an official form of Veteran ID, they may not accept it (and Veterans will be angry/disappointed/inconveniences in that moment, but it might also erode trust in VA & the app).
4. We don't currently coordinate with VA comms team when we launch features.
5. There are [several other forms of ID that are currently accepted and used to get discounts](https://www.va.gov/records/get-veteran-id-cards/vic/)(Veteran Health Identification Card (VHIC), Department of Defense (DoD) Identification Card—either a Common Access Card (CAC) or Uniformed Services ID Card, or a state-issued driver’s license or ID with a Veterans designation), and Veterans may find it easier to use those instead.

### Business Goals
- Increase app downloads overall
  - Bring users into the app that do not use VA Health
- Increase overall number of app active users
  - Give non-Health users a reason to return to the app
- Relates to [OCTO-DE goals:](https://github.com/department-of-veterans-affairs/va.gov-team/tree/master/strategy#readme)
   - Logged-in users have a personalized experience, with relevant and time-saving features
   - Increase Veteran satisfaction with VA (Allowing Veterans to have a digital ID, which is highly requested and desired)



### Roadmap

#### V1
* 
#### V2 and beyond**
* 

### Technical Approach
* Unique identifier?
* Discharge status API
* Is there a way to access which Veterans have VICs and just surfacing it in the app?
* ID needs to be available offline
* Must have non-dishonarable discharge

### Measuring success
#### Usefulness of VIC:
* Track number/% of Users that access the ID in the app
* Track number/% of users that regularly access the ID in the app over time
* OS Wallet metrics for how often IDs in the Wallets are accessed?  
   * Location of where/when it is accessed in wallet?
#### Impact of launching VIC:
* An increase in app downloads that correlates with the launch of VIC card
* An increase in the overall number of active app users
    * An increase in usage of the app by users who do not currently use Health tools
    * An increase in overall usage of the app that correlates with the usage of VIC card in the app
* An increase in Veteran's satisfaction with VA that correlates with VIC card usage and/or the presence of VIC card  in the app
* Requests for ability to provide proof of service decreases in [need to understand where these requests are happening now]
   

### Stakeholders
* Melisa Rebstock (VEO)
* Joe Valentine (with Angela Gant-Curtis) - Technical contact for VIC
* Molly Burlage - VIC Lead
* John Lundy - division cheif VEO


### Potential Solutions
1. Surface official VIC within the app
   1. Could work to make request process smoother, including submitting a photo
   2. This would involve working with a VA group that may not have APIs to support what we need.  We may need to help build them ourselves.
   3. Could try adding a version of it to the OS Mobile Wallet
2. Create a separate ID card within the app that serves the same purpose but doesn’t adhere to the VIC regulations
   1. Need to ensure the ID we create would be accepted by external groups
   2. Could add it to the OS Mobile Wallet
   3. Discussion
      1. We wouldn’t do the photo which would be against the law
      2. No need for an application
      3. Risks
         1. Stakeholders - VEO
         2. Very different than web
         3. How do we guarantee that outside orgs will take the ID? - not sure, should talk to them

### Open Questions
**Questions for existing VIC:**
* Is there an API to find which Veterans have a VIC?
* Applying for VIC:  
  * 2 ways to apply, AccessVA or VA.gov but VA.gov isn't working right now
  * apply online, login.gov doesn't work yet but 
  * upload gov ID and photo and maybe DD214
  * Mobile version might not need the photo
    * Have asked Congress to remove requirement for photo
  * once 'approved' they are sent an image
    * Confirming Gov ID, approve photo
  * There is an ID #
* Can we access the VIC PDF and surface it (or ideally the data used in the PDF) in the app?
* Who would we work with in VA for this?
* What does their audience look like now?  How many Veterans have a VIC?
* Can Veterans print the card on their own, at home? Or does it have to be printed a specific way?
* In what specific real-life situations does the VIC card get used today?
    * What are the discounts and other private-sector benefits Veterans would have access to with their VIC?
    * How frequently do Veterans need to use some form of Veteran ID?
    * Do we have contacts at Home Depot, Lowes, etc. to ensure they would accept any ID card we make that is separate from the VIC?
      * They had to do Comms to get stores to accept it.  Many do their own credentialing. 
      * Not TSA standards, VHIC can be
      * VHIC used to be called VIC so there is naming confusion - VA Employees still call VHIC VIC sometimes
      * Just stopped doing physical cards last October

**Questions for creating our own digital VIC:**
* Is there a way to make a digital VIC ‘official’ with the VA, and therefore would be accepted by 3rd parties?
* What sort of outside communications and coordination would be required to ensure that digital VIC is an accepted form of Veteran identification?
* Are there other VA stakeholders we should work with if we create our own?
* Are there any other VA cards we could add to the OS Mobile Wallet?  VHA card, etc.?
    * Vaccine ‘card’?

### Important Links
- Google Wallet: [Google Wallet](https://wallet.google/#identity)
- iOS Wallet: [IDs in Wallet](https://learn.wallet.apple/id)
- [How To Apply For A Veteran ID Card](https://www.va.gov/records/get-veteran-id-cards/vic/)
- [H.R.91 - 114th Congress (2015-2016): Veterans Identification Card Act 2015](https://www.congress.gov/bill/114th-congress/house-bill/91) 
- [Military Info, Profile Research Findings - Office of the CTO - Digital Experience (OCTO-DE), Profile, Authenticated Experience - 03/20203](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/profile/military-information/discovery-and-research/2023-military-info-discovery/findings-summary.md#military-info-profile-research-findings)


### Notes from VIC Meeting
- Melissa to send Research they did and metrics from last 3 years
  - existing process and pain points
  - How many applications are rejected
  - Confusion with VIC and VHIC

- Don't call it VIC 
- Average 350 cards a day, Veterans Day has as many applications as month
- They had done their own research on who gives Veteran Discounts and just called them to tell them to take the ID

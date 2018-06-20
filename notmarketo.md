2018.06 - a large manufacturing company based in Portland, OR

Another marketing integration. This time it's using Marketo and SQL Server. I have never been so far removed 
from the actual application than this particular integration. It's one thing to visualize how an application 
works, but to integrate it as a 3rd party for 2nd party usage? That's a first.

As with any big enterprise company, customer privacy is really important in how we build processes that handle that type of data.

Marketo is the distribution vehicle for B2B customer emails that promote an offer based on a product application type.

The part that is truly baffling about this integration is how we are managing uploaded customer data. For one, internal IT is building
a custom web form so that designated dealers in our dealer network can upload customer lists. That data is stored in SQL Server
and then our marketing agency takes those flat files and transfers them to Marketo, fills the broadcast funnel, and pushes emails
out to their respective campaign themes and matching landing pages.

Umm, WTF.

If, on the other hand, we had our own instance of Marketo, we would be able to set this up with minimal interference from both
the marketing agency and IT. I mean heck, Pardot has this feature. I would imagine Marketo does as well, being that it is the 
pricier version of enterprise marketing automation.

I had originally envisioned this campaign as follows:

Build a lead gen form in Marketo and its related campaign landing pages. Allow 'users' to upload customer data (name, email address, phone, etc.) and select a campaign email theme
(one of four possible options), create a giant funnel that would automatically segregate the customer data based upon which email theme
was chosen, and then broadcast on a drip schedule of every other week for a finite number of emails.

If we were extra clever, we would build skip logic into that drip flow and remove the customer prospect from the drip if they had 
successfully completed one of two actions: get a quote from a dealer or demo a unit.

Alas, none of that is happening.

Instead, we are building a non-Marketo web form that stores data in a secure SQL Server, exports out 'leads' in a 
csv format on a daily basis for our marketing agency to then upload into Marketo.

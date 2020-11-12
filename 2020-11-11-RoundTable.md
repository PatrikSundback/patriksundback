## RoundTable 2020 Patrik Sundbäck iOS Developer 
### Reflections on my delivery 2020
In this composition I will bring forth three projects I worked on this year where all have different flavors and are strong candidates to reflect upon.

### C More Kids profiles & themes - November 2019
A new kids friendly content mode with customizable avatars and colorful themes. Choose content for toddlers ages 0 to 6 or older children.

#### What I worked on
* A profile network service. Using C More GraphQL networking for profiles data as well as creating, editing and deleting profiles.
* A profile manager which provides the kids mode with all needed data for example current and available profiles & themes. 
* An improved UserSession service which integrates the profile service and provides data for user & authorization.
* Kids content pages with customizable theme & avatar layout for tvOS as well as choose or edit/customize profiles pages.
* An orientation handler for constraining and managing transitions between portrait and landscape.

#### The Kids project
The kids project was a cross platform project where the Backend, GraphQL, Web, iOS, Android & UX teams worked together in a designated project room. We had daily cross platform standups where QA, Analytics and Product teams also joined in. Patrik and Caleb represented the iOS team at a beginning and grew with another iOS consultant. Jenny also joined in to help build kids for iOS. Working in a cross platform project was a great experience where we had direct and open communication with all teams. The knowledge spread was instant between the developer teams and we had no barrier for questions. This was important since the project was quite pressured by a very tight deadline with a continuously changing final product and where the priorities between scope and deadline were not agreed upon from stakeholders.

#### Reflections on my project contribution
My approach was to value the project as a whole where success was measured by the result of the project across all platforms. A brand should feel the same for a user across the Web, iPhone, tvOS and Android. I took a responsibility in being transparent and communicating important information across all teams.
 
Early in the project Caleb and I defined what needed to be done in the iOS team, what should be prioritized and what could possibly be scoped out. We had discussions with the UX team in order to agree on scope and adjustments which we then communicated in our standups. We also planned for integration with the ongoing Downloads project to make sure our projects would not block each other. 
 
I defined what we needed from GraphQL and had continuous communication with the GraphQL team on data structure. To get a heads start and simplify development for the iOS team I created mocked data and continuously replaced it with real data when available. This way we could start development of the Kids pages as early as possible without needing to wait for the GraphQL data. With this approach I could detect edge cases early which I made sure all platforms communicated so we could take unified decisions. An example of this was an edge case on how to handle an active profile in iOS & Android when that profile was deleted from the Web.
 
Since we got a heads start I could support the Android team with our solutions regarding GraphQL questions. Our team could raise flags early on which started important discussions and awareness in time. For instance limits of the new font for kids.
 
With the tight deadline and the fact that the iOS team had to build the kids feature for both iOS and tvOS we took responsibility on building modular and reusable code that could be used on both platforms. I also felt a responsibility at times to indicate focus and break over engineering. For instance I would onboard our new consultant to quickly get on track with helping our team. During stressful times with a lot of things to do there may be tendencies for some to feel a need to rewrite old features that already work into a pattern they feel suits better. This is great when discussed and decided within our entire iOS team to raise discussions and plan for a process, but this can also be damaging if not communicated and could shift focus on wrong things. These decisions should not become a "rogue decision" and I emphasised where the line should be in the Kids project to help our consultant focus on related features.

### CoreTracking with Firebase - January 2020
A standardized tracking across Web, iOS and Android led by the Analytics team.

#### What I worked on
* A CoreTracking framework for iOS & tvOS to be used by C More, TV4 Play and possible future brands.
* Integrating the custom built Firebase_tvOS_SDK from Lars Rothaus
* A continuous integration strategy for tests and easy framework updates.
* Specification and documentation on tracking pages.
* Documentation on how to debug tracking.

#### The CoreTracking project
This project was initiated by Alexander Bergqvist chief of Analytics and led by David Jurelius from the Analytics team. They specified key KPI metrics and from that designed a unified tracking for all platforms. David wrote a documentation covering all needed tracking events and parameters that we should implement. We had weekly stand ups with representatives from iOS, Android and Web teams for questions and limitations.

#### Reflections on my project contribution
When designing the CoreTracking framework I wanted to make it easy and intuitive for iOS developers to use so I started with design principles and created a "architecture proposal" documentation. During the making of this proposal I had discussions with Jenny and Per-Jan for help with intuitive naming conventions. When the proposal was finished I had a meeting with the iOS Team to discuss and agree upon design principles in order to let the entire team be a part of the decisions.
 
I started defining what needed to be done from the iOS team as early as possible as well as understanding what the tracking events workflow really meant to find possible edge cases. This resulted in early discussion with David Jurelius and clarified what actually was needed in the tracking parameters. For instance our discussions led to a conclusion that most of the parameters were not needed on assets and panels tracking since that information could be gathered from BigQuery by using asset.id & panel.id. 
 
As the basics of the CoreTracking framework was near completion Jenny joined to help with implementation of the framework on TV4 Play. The onboarding went smooth and during onboarding our discussions resulted in architecture improvements. We could easily start working on implementing CoreTracking for C More and TV4 Play. At the final stages Jenny took over the project and I had a handover meeting for the entire iOS Team on how to develop on CoreTracking.
 
When returning from parental leave I continued working on CoreTracking and contacted Lars regarding a tvOS tracking bug. I had a takeover learning period with him on how to work with the custom Firebase_tvOS_SDK and learned how to fix bugs and re-compose the framework. I shared my knowledge with Marcus Norling when we fixed crashlytics for iOS and tvOS.
 
### OneApp structure - November 2020
This feature we all know :)

A way of working by sharing pattern principals, building reusable services & layout elements in order to unite the C More & Telia apps.

#### What I worked on
* Pattern discussions & suggestions.
* Supporting knowledge such as the GraphQL environments and authentication & personalisation.
* Sport refactoring with MVVM and coordinators.
* Refactoring pages in C More to use coordinators.

#### The OneApp project for iOS
The OneApp iOS refactoring development started by Magnus Thoor and Magnus Nilsson with a proof of concept project which is used as a template for the rest of the iOS team. They initiated design patterns such as an AppContext of services, navigation through coordinators and testable data logic through MVVM. Slowly but steady members of the iOS team are introduced to the OneApp way of working and with open discussions and proposals the solutions emerge organically. 

#### Reflections on my project contribution
First of all I want to emphasize my excitement regarding this project, our team has had several discussions and attempts to bring forth patterns which all have failed to bear fruit. I will now more than ever keep aspirin to help raise our code to become an intuitive and testable base which becomes more flexible and easy to build upon. 
 
The work I've done so far has either been in pair programming or pair reviewed which resulted in knowledge sharing and a more thoughtful process which brings forth good ideas. In this project I've gotten a good feel for the benefits of working in pairs and hope this way of working will raise the knowledge of our entire team and perhaps even contribute to a sense of a community.
 

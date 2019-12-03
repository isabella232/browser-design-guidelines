
# IPFS Browser Design Guidelines

In preparation for a 2020 expansion of Protocol Lab’s IPFS browser integrations and standardisation efforts, there needs to be guidelines and recommendations on hand in order to get to our first billion users.

### What the guidelines are

The IPFS Browser Design Guidelines will be an implementation kit for browser security and design teams and for standards groups such as the W3C and IETF. It will contain research, use-cases, UX patterns, and examples of iconography. This implementation kit for IPFS will be specifically tailored to how browser URL bars are implemented today.

### How the guidelines will be used

Initially this material will guide Protocol Labs’s own projects (Desktop, Companion). Additionally, it will help guide the smaller and more experimental browser implementations where we can learn, test and iterate. That will set us up for working with larger browser vendors and the standards groups later in 2020, putting this material to use in broader ways.

## Research

While the browser landscape has never been bigger, with increased specialisation in terms of privacy or blockchain, there doesn’t seem to be any investigation or development in terms of P2P or distributed enabled browsers. 

The intent of the research phase is to examine and explore the use-cases for IPFS in browsers, P2P usage in browsers at large in order to create and publish design guidelines and recommendations for browser vendor implementation and standards bodies.

### [Survey review](https://github.com/ipfs/browser-design-guidelines/wiki#browser-survey)

One of the first things to research was the (existing browser landscape)[https://github.com/ipfs/browser-design-guidelines/wiki#browser-survey], in this case concentrating primarily on current (2019-Nov) releases of Mozilla Firefox, Apple Safari, Google Chrome and Microsoft Edge, the aim of which was to establish the commonalities and baselines between the current browser stack. From this we could continue into exploring in detail through user research what works and what doesn’t with that.

### [Exploratory workshop](https://github.com/ipfs/browser-design-guidelines/wiki/Stakeholders-workshop)

An expert/stakeholder workshop was conducted in conjunction to the ongoing expert interviews to explore the problem space, relevant technology and possible solutions.

The user research was split into three parts. The first was an (exploratory and scoping workshop)[https://github.com/ipfs/browser-design-guidelines/wiki/Stakeholders-workshop] with three key developers of IPFS to look at where the leading developmental issues may lay.

### [Non-expert research](https://github.com/ipfs/browser-design-guidelines/wiki#non-expert-interviews)

Afterwards, the second phase was non-expert research with average users, in this case defined as non-developers or people working on internet protocol level issues. This covered their browser use, their understanding of location and addressing in the browser and knowledge and opinion on P2P in general.
99
We conducted research with seven participants, spread geographically and across genders and occupations to determine their conceptions, concerns and ideas about addressing conventions and P2P technologies in modern browsers. In depth interviews with notes and findings are found in the (wiki)[https://github.com/ipfs/browser-design-guidelines/wiki].

### [Expert research](https://github.com/ipfs/browser-design-guidelines/wiki#expert-interviews)

Lastly, a small cohort of expert users involved directly with P2P or IPFS development, cryptography or browser development were interviewed to gather specialist knowledge and opinions on the domain and technological and user landscape. In depth interviews with notes and findings are found in the [wiki][8].

## Research findings

### Initial assumptions

- The URL as a mechanism and way to understand location on the Internet is fairly well understood and usable
- A URL is at least partially human-readable by most people
- Privacy and encryption is a concern for the majority of users but many if not most don’t explicitly care where the data comes from, just as long as it’s authentic or credible
- What is going on in a browser with privacy and a secure connection is largely understood
- Domains are signs of trust and at least partially comprehended in terms of what is going on, for instance .com, .org, etc.
- P2P in a browser is largely only understood by developers
- P2P (and IPFS) is easy to understand
- The use cases of P2P in terms of a browser are clearly understood

### Research findings

- The URL is only important as a backup and source of credibility that the right things are happening in the browser
- The URL bar as it is presented now is probably fine just the way it is
 - Although the URL or what is happening in the URL bar may not be widely understood, nobody wants it to go away as it serves as a semi-readable source of authenticity, for instance at a domain level
- Almost across the board between non-experts and experts, URLs are rarely typed in and the URL bar is used for search as a primary means of navigation
- A few research participants use autocomplete with domains and finding URLs via history and bookmark functions in their browser
- The time is right to look at new modes of privacy, use and control on the Web. Privacy and security are a great concern to users, both expert and non-expert, however, it is not greatly understood by non-experts and they often have misconceptions and are thus largely left feeling hopeless about it
 - Users at large are overwhelmed if not defeated by ads, tracking, surveillance and privacy concerns
 - HTTPS is something all users are aware of although they might not fully understand it’s implications
- People have issues with long URLs and in particular ones that seem to have what are perceived to have codes or tracking things in them
- Blogs have given people a better understanding of URLs
 - The URL is perceived to be potentially very useful if it had certain standard conventions or features such as having topic, author or title included
- There have been attempts in browsers, particularly with Microsoft and Internet Explorer, to bring a clickable interface to the URL
- P2P is largely understood to be about files that are in many places at the same time by many people, but is largely thought of by non-experts as a tool for media piracy which could have potentially given a good technology a bad name
- How files and folders work in P2P, especially in terms of the URL isn’t greatly understood by both non-experts and experts
- Most assume P2P makes things faster and somehow more secure
- Privacy as a concept on the Internet is understood differently in different parts of the worlds
- When in P2P ‘mode’, it may be very beneficial to the user to have a drastically user or visual experience to differentiate the mode of use
- There are potential opportunities with P2P in terms of lowering CDN costs and lessening or eliminating the need for invasive advertising
- P2P might be better suited to use that is more niche and not mass scale, such as scientific and academic publishing
- Incentivisation and participation models need to be explored much more and better communicated

#### Key design and user context questions and issues

- How might we design P2P (IPFS) to be used by the wider browser user base in terms of accomplishing a typical user tasks easier than they do now, for instance sharing photos?
- How might we clearly communicate the benefits of using P2P technologies?
- How might we set the context for a range of users in quickly orienting people as to what they are doing without overwhelming them or showing them the actual working of the protocol?
- How might we allow the user be enabled to participating in a P2P scenario by being stepped through the first few times?
- How might we communicate to the users visually what is happening?
- How might we explore niche use cases such as scientific and academic publishing?
- How might we better understand where context, location and culture is important in perceptions of privacy, participation and P2P?
 - How might we explore design in which P2P is used or explained with public folders like with Dropbox?
- How might we think of a repository-type approach in thinking about distributed content stores?
- How might we we ensure trust and verification of content ownership and security fo users when connecting to other people’s computers and devices?
 - How can we incentivise users with some reward in P2P, for instance a page giving the user no ads in return for participation?

## Design

The intent of the design phase of the IPFS Browser Design Guidelines is to examine and explore the use-cases for IPFS in browsers, and publish design guidelines and recommendations for browser vendor implementation

### Hypotheses

#### An uncomplicated, unobtrusive P2P GUI with deeper, hidden levels of control will help experienced but non-developer users
Know that they are participating in P2P in a safe and trusted manner.

We will know this is valid when users understand they are participating in P2P without being told and feel okay with it

&nbsp;

#### We believe that showing the user a clearly communicated value proposition to use P2P will help curious browser users
Onboard to and begin using P2P protocols

We will know this is valid when users report the benefits of partipating in P2P and continue using

&nbsp;

#### We believe that having a way to see the authenticity and safety of the content shared will help P2P users who are concerned about privacy and surveillance
Continue to use the protocol

We will know this is valid when P2P users are shown to be using this initially a lot but in decreasing amounts throughout their continued use

&nbsp;

#### We believe that seeing an easily understandable first time process for beginning to participate in P2P will get non-expert users
To quickly onboard and only use this once

We will know this is valid when data or research shows that it is being used only once

&nbsp;

### Programme of work

- Interaction and user experience design work to solve the researched issues, mapping out user flows, design patterns and use cases
- Interface design

### Deliverables

- Screen designs including recommendations, iconographic and design treatments for existing browser URL bars
- User experience flows
- Design guidelines and component design to inform and help further development efforts
- Recommendations for further work

---- 

#### Credits

Free stuff used in this repo

Icons: (Font Awesome)[https://fontawesome.com/]

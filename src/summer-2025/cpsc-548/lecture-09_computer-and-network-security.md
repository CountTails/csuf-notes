# Lecture 9: computer and network security

## Hacking

**Hackers**

- Original meaning: MIT's tech model railroad club in 1950's (explorer, risk taker, system innovator)
- Modern meaning: someone who gains unauthorized access to computers and computer networks

**Obtaining login IDs and passwords**

- Eavesdropping
- Dumpster diving
- Social engineering
- Use of stolen or guessed passwords

**Password dos and don'ts**

- Long password
- Special characters
- No dictionary word
- Change it regularly
- Use 2FA

**Computer fraud and abuse act**

- Criminalizes wide variety of hacker-related activities and computer fraud
- Maximum penalty
  - 20 years in prison
  - $250,000 fine

### Sidejacking and firesheep

**Sidejacking**

- Hijacking of open web session by capturing a user's cookie
- Possible on unencrypted wireless networks because many sites send cookies "in the clear"
- Internet security community complained about sidejacking vulnerability for years, but e-commerce sites did not change practices

**Firesheep extension to Firefox browser**

- Released in 2010 by Eric Butler
- Made it possible for ordinary computer users to easily sidejack web sessions
  - More than 500,000 downloads in the first week
  - Attracted a great deal of media attention
- In early 2011, major sites announced options to use their sites securely

## Malware

**Virus**

- Self replicating code embedded within another program (host)
  - Hosts are program files on disk
  - Spreads through disk devices, email attachments and internet downloads
- Be careful with fake free antivirus packages

**Worm**

- Self contained program
- Spreads through a computer network, exploits security holes in networked computers
- Famous case of internet Worm
  - Cornell graduate student releases internet Worm
  - Spread to many Unix computers and made them keep crashing or become unresponsive
  - Took a day for fixes to be published
  - Impact on student
    - Suspended from Cornell
    - 3 years probation
    - 400 community service hours
    - $150,000 in legal fees and fines

**Cross-site scripting**

- Downloaded without user's knowledge through injected script on a page
- Victim's browser executes scripts, which may steal cookies, track user's activity, or perform other malicious action

**Drive-by downloads**

- Unintentional downloading of malware from a compromised website
- Pop up window asking permission to download software and clicks "Okay"

**Trojan horses and backdoor Trojans**

- Trojan horse: a program with benign capability that masks a sinister purpose
- Backdoor Trojan: gives attack access to victim's computer

**Rootkit**

- Set of programs that provides privileged access to a computer

**Spyware and adware**

- Spyware is a program that communicates over an internet connection without user knowledge or consent
  - Monitors web surfing
  - Logs keystrokes
  - Take snapshots of computer screens
  - Sends reports back to host computer
- Adware is a type of spyware that displays pop up advertisements related to user's activity
- Backdoor Trojans often used to deliver spyware and adware

**Bots, botnets, bot herders**

- Bot is a kind of backdoor Trojan that responds to commands sent by a command-and-control program on another computer
  - First bots supported legitimate activities
  - Other bots supported illegal activities
- Botnet is a collection of bot-infected computers controlled by the same command-and-control-program
- A bot herder is someone who controls a botnet

### Defensive measure for malware

- Security patches to remove security vulnerabilities
- Anti-malware tools to
  - Scan hard drives
  - Detect files that contain viruses or spyware
  - Delete these files
- The fight between malware and defensive measures will continue

## Cyber crime and cyber attacks

- Criminal organizations making significant amounts of money from malware
- Jeanson James Ancheta
  - Created a network of ~400,000 bots including the computers operated by the US department of defense and sold it to Adware companies, spammers, and others
  - Pleaded guilty to a variety of charges after being arrested by the FBI
- Pharmamaster: blue security vs. spammers
- Albert Gonzalez
  - Used an SQL injection attack to steal more than 130 million credit and debit card numbers
  - Sentenced to 20 years of imprisonment
- Avalanche Gang: name given to the criminal enterprise responsible for more phishing attacks than any other organization

### Internet based attacks

**Phishing**

- Large scale effort to gain sensitive information from gullible computer users
- Spear fishing: variant of phishing in which email addresses chosen selectively to target a group of recipients

**SQL injection**

- Method of attacking a database driven web application with improper security
- Attacker inserts (injects) SQL query into text string from client to application

**Denial-of-service (DoS) attack**

- Intentional action designed to prevent legitimate users from making use of a computer service
- Distributed DoS attacks are launched from many computers, much like a botnet

### The rise and fall of Blue security

- The rise
  - An Israeli company selling a spam deterrence system
  - Blue Frog bot would automatically respond to each spam message with an opt-out message
  - Spammers started receiving hundreds of thousands of opt-out messages, disrupting their operations
  - 6/10 of world's top spammers agreed to stop sending spam to users of Blue Frog 
- The fall
  - PharmaMaster started sending Blue Frog users 10-20 times more spam
  - PharmaMaster then launched DDoS attacks on Blue Security and its business customers
  - Blue Security could not protect its customers from DDoS attacks and virus-laced emails
  - Blue Secuirty reluctantly terminated its anti-spam activities

### Political motivation

**Estonia**

- Moved a symbolic statue to a Russian military cemetery in suburbs
- Massive DDoS attack

**Georgia**

- Twitter service unavailable for several hours on August 6, 2009
- Facebook, LiveJournal, and Google were attacked on the first anniversary of ware between Georgia and Russia
- All sites were used by a political blogger from the Republic of Georgia

**Exiled Tibetan government**

- Backdoor Trojan for surveillance targeting the Dalai Lama and some Tibetans

**United States and South Korea**

- On 4th of July weekend in 2009, DDoS attack on governmental agencies and commercial websites in US and South Korea
- Attacks may have been launched by North Korea in retaliation for United Nations sactions

**Iran**

- Industrial processes require constant monitoring
- Computers allow automation and centralization of monitoring
- Supervisory control and data acquisition (SCADA) systems are open systems based on internet protocol
  - Less expensive than proprietary systems
  - Easier to maintain than proprietary systems and allow remote diagnostics
  - Allowing remote diagnostics creates a security risk
- Stuxnet worm attacked SCADA systems in Iran and caused a temporary shutdown of IRan's nuclear program
- Some evidences points Israeli Defense Forces

**Espionage attributed to People's Liberation Army**

- Hundreds of computer security breaches in more than a dozen countries investigated by Mandiant
- Hundreds of terabytes of data stolen
- Mandiant blamed unit 61398 of the People's Liberation Army
- China's foreign ministry stated that accusation was groundless and irresponsible

**Anonymous**

- Loosely organized international movement of hacktivists (hackers with a social or political cause)
- Various DDoS attacks attributes to Anonymous members

| Year | Victim | Reason |
| ---- | ------ | ------ |
| 2008 | Church of Scientology | Attempted suppression of TOm Cruise interview |
| 2009 | RIAA, MPAA | attempt to take down the Pirate Bay |
| 2009 | PayPal, VISA, MasterCard | Financial organizations freezing funds flowing to Julian Assange of WikiLeaks |
| 2012 | US Dept of Justics, RIAA, MPAA | US Dept of Justice actions against Megaupload |

## Online voting

- Motivation for online voting
  - 2000 US presidential election closely contested
  - Florida was the pivotal state
  - Most Florida counties used keypunch voting machines
- Two voting irregularities traced to these machines
  - Hanging chad
  - "Butterfly ballot" in Palm Beach County

### Benefits

- More people would vote
- Votes would be counted more quickly without ambiguity
- Cost less money
- Eliminate ballot box tampering
- Software can prevent accidental over-voting and under-voting

### Risks

- Gives unfair advantage to those with home computers
- More difficult to preserve voter privacy
- More opportunities for vote selling
- Obvious target for a DDoS attacks
- Security of election depends on security of home computers
- Susceptible to vote-changing virus
- Susceptible to phone vote servers
- No paper copies of ballots for auditing or recounts

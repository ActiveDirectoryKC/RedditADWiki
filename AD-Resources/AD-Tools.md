>❗❗❗\[WARNING\]❗❗❗
>Many of these tools WILL trip EDR/XDR, ITDR and any intrusion detection scanners. Some of the information gathered is the same information that malicious actors would want to gather. Make sure you communicate with your security team and SOCs before running these tools. You've been warned.

This is a collection of scripts, tools, and general tools that the community has found helpful for Active Directory. We will try to keep this list updated and new tools as we find them. If you think of something that should be added, send a [modmail ](https://www.reddit.com/message/compose?to=r/activedirectory)or post an [issue](https://github.com/ActiveDirectoryKC/RedditADWiki/issues) on the wiki's github and we'll get it added. Likewise if a link is broken let us know.

This page is vaguely organized based on tool function with as much information as we can realistically provide in this kind of format. If you have comments or feed back, please [message the mods](https://www.reddit.com/message/compose?to=r/activedirectory).

In addition, all r/ActiveDirectory wiki pages and resource posts (which are duplicates of the wiki pages) are stored on GitHub: [](https://github.com/ActiveDirectoryKC/RedditADWiki)

If you are interested in how these items were selected see the wiki page for [AD Tools Reviews Guidelines](https://www.reddit.com/r/activedirectory/wiki/index/Tools-And-Resources-Listing-Guidelines). This is also where you can get details on submitting your script or tool.


>!**ICONS REFERENCE**!<

* >!💥- Resources that are guaranteed to trip the SOC monitoring and are likely to be detected by AV/EDR.!<
* >!❗ - Resources that are going to trip SOC notifications. Coordinate with your SOC team.!<
* >!✨ - Resources that are highly recommended by the community and reviewed by Mods.!<
* >!❔ - Indicates that the resource is recommended by community members but not fully reviewed by mods.!<


# Script Collections

* ✨DSInternals
   * One of the best collections of AD scripts and tools ever created.
   * [https://github.com/MichaelGrafnetter/DSInternals](https://github.com/MichaelGrafnetter/DSInternals)
* ✨Jorge's Script Repo
   * [https://github.com/zjorz/Public-AD-Scripts](https://github.com/zjorz/Public-AD-Scripts)
   * Jorge is known for his years as an MVP and his great tools. He wrote the Krbtgt reset tool that Microsoft still pushes (not his newer version is better).
   * ✨Reset-KrbTgt-Password-For-RWDCs-And-RODCs.ps1
      * [https://github.com/zjorz/Public-AD-Scripts/blob/master/Reset-KrbTgt-Password-For-RWDCs-And-RODCs.ps1](https://github.com/zjorz/Public-AD-Scripts/blob/master/Reset-KrbTgt-Password-For-RWDCs-And-RODCs.ps1)
* ✨EvotecIT ADEssentials
   * Evotec has been pumping out great scripts for years and any tool from them should be used.
   * [https://github.com/EvotecIT/ADEssentials](https://github.com/EvotecIT/ADEssentials)
* ✨GPOZaurr (EvotecIT) - Group Policy Eater is a PS module that aims to gather information about GPOs and issues.
   * [https://github.com/Group3r/Group3r](https://github.com/Group3r/Group3r)
* ✨GPOMigration Scripts - Useful for exporting your policies and uploading them into a new domain.
   * [https://github.com/GoateePFE/GPOMigration](https://github.com/GoateePFE/GPOMigration)
* ✨PSPKI Module - Module simplifies many of the varies PKI and AD CS management tasks.
   * [https://github.com/PKISolutions/PSPKI](https://github.com/PKISolutions/PSPKI)
* PSPKIAudit - Tool for auditing AD CS
   * [https://github.com/GhostPack/PSPKIAudit](https://github.com/GhostPack/PSPKIAudit)
* 💥AADInternals - Tools for administering Entra ID (Azure AD) and Office 365
   * [https://github.com/Gerenios/AADInternals](https://github.com/Gerenios/AADInternals)

# Scanning and Auditing Tools

* ✨MS Security Compliance Kit
   * [https://www.microsoft.com/en-us/download/details.aspx?id=55319](https://www.microsoft.com/en-us/download/details.aspx?id=55319)
   * The starting point for any AD Security program.
* ❗✨Purple Knight (Semperis)
   * This is a free tool by Semperis that does a very comprehensive health check. Also checks PKI. This is a must run in every AD where you can run it.
   * Requires an email address which will get you a little bit of emailing from Semperis. Not too much compared to others and not tons of plugs for their paid software.
   * WILL PRVOKE EDR/IDTR SOLUTIONS!!! This does a lot of scans so many solutions will flag the activity.
   * [https://semperis.com/downloads/tools/pk/PurpleKnight-Community.zip](https://semperis.com/downloads/tools/pk/PurpleKnight-Community.zip)
* ❗ Forest Druid (Semperis)
   * Another Semperis tool in line with Purple Knight, but this one focuses on securing highly privileged accounts (Tier 0 \[Domain Admins\]). Affectionately referred to as "Bloodhound lite".
   * Would get a higher rating (stars) but it is a bit clunky to use and not super useful user-friendly.
   * [https://semperis.com/downloads/tools/fd/ForestDruid-Community.zip](https://semperis.com/downloads/tools/fd/ForestDruid-Community.zip)
* ❗ PingCastle (Netwrix)
   * This is a freeium scanning tool that can give you at least a base-level security posture for your environment.
   * Netwrix is a little spammy with their products but recently-ish acquired PingCastle so we'll see where it goes..
   * [https://www.pingcastle.com/download/](https://www.pingcastle.com/download/)
* ✨Locksmith - [https://github.com/jakehildreth/Locksmith](https://github.com/jakehildreth/Locksmith)
   * PKI Auditing and Checking Tool.
   * This is a must have when running PKI. Really good and there is a lot of active development on it (2025).
* ✨BlueTuxedo - [[https://github.com/jakehildreth/BlueTuxedo](https://github.com/jakehildreth/BlueTuxedo)
   * "A tiny tool built to find an dfix common misconfigurations in AD-Integrated DNS..."
   * Finds stuff in DNS you may not find.
* 💥BloodHound/SharpHound - Attack Path Analysis
   * [https://github.com/BloodHound](https://github.com/BloodHound)
   * Almost every EDR/XDR/ITDR tool will pick up on this and alert. Be warned.
* GoodHound - actionable lists from BloodHound - 
   * [https://github.com/idnahacks/GoodHound](https://github.com/idnahacks/GoodHound)
* Adalanche - AD ACL Explorer/Visualizer
   * [https://github.com/lkarlslund/Adalanche](https://github.com/lkarlslund/Adalanche)
* Trimarc AD Checks - Sean Metcalf (ADSecurity.org)
   * [https://www.hub.trimarcsecurity.com/post/securing-active-directory-performing-an-active-directory-security-review](https://www.hub.trimarcsecurity.com/post/securing-active-directory-performing-an-active-directory-security-review)
   * Trimarc has been absorbed by TrustedSec so the links may change.
* Invoke-TrimarcADChecks (Trimarc)
   * [https://github.com/Trimarc/Invoke-TrimarcADChecks](https://github.com/Trimarc/Invoke-TrimarcADChecks)
   * Trimarc has been absorbed by TrustedSec so the links may change.
* AD ACL Scanner - 
   * [https://managedpriv.com/project/ad-acl-scanner/](https://managedpriv.com/project/ad-acl-scanner/)
* ScriptSentry 
  *  [https://github.com/techspence/ScriptSentry](https://github.com/techspence/ScriptSentry)
  *  Helps identify and find dangerous logon scripts.
* ADeleginator
   *  [https://github.com/techspence/ADeleginator](https://github.com/techspence/ADeleginator)
   *  Helps identify and find dangerous AD trustee and resource delegations.
*  ❔Harden-Sysvol
   *  https://github.com/dakhama-mehdi/Harden-Sysvol
   *  "HardenSysvol is an open-source tool developed by the HardenAD Community to complement Active Directory audit tools by analyzing GPOs and scripts on Sysvol folder."

## Generic Scanning / Vulnerability Tools
* Wazuh - Open Source SIEM/XDR Solution
  * https://wazuh.com/
  * AD-specific Configurations
    * https://wazuh.com/blog/how-to-detect-active-directory-attacks-with-wazuh-part-1-of-2/
    * https://wazuh.com/blog/how-to-detect-active-directory-attacks-with-wazuh-part-2/
* Hardening Kitty - CIS benchmarking script
   * [https://github.com/scipag/HardeningKitty](https://github.com/scipag/HardeningKitty)
* OpenVas - General Vulnerability Scanning Tool (Similar to Nessus or Rapid7)
   * [https://www.openvas.org/](https://www.openvas.org/) (like Nessus but free)

# General Tools

* ✨AD Repl Status (Ryan Ries)
   * [https://github.com/ryanries/Adreplstatus](https://github.com/ryanries/Adreplstatus)
   * While not a "security tool" it is hard to not recommend this tool.
* ✨\[LEGACY\] Microsoft Account Lockout Tools
   * [https://www.microsoft.com/en-gb/download/details.aspx?id=18465](https://www.microsoft.com/en-gb/download/details.aspx?id=18465)
   * These are the original lockout tools provided by Microsoft ages ago.
   * EventCombMT is a great tool for log gathering if you don't a central repo.
   * LockoutStatus will display the lockout status of users against different DCs. The pre-built options use the old event IDs and you'll need to change this.
* ✨Lingering Object Liquidator (LoL)
   * [https://www.microsoft.com/en-us/download/details.aspx?id=56051](https://www.microsoft.com/en-us/download/details.aspx?id=56051)
   * Tool used to clean up lingering objects.
* 💥 AdFind (Joeware)
   * [https://www.joeware.net/freetools/tools/adfind/index.htm](https://www.joeware.net/freetools/tools/adfind/index.htm)
   * An AD Searcher tool that is very robust and predates PowerShell. Still being activity developed.
   * This will trip most AV/EDR solutions as the bad guys are using it because it is so good. That is why it isn't starred.
* 💥 AdMod (Joeware)
   * [https://www.joeware.net/freetools/tools/admod/index.htm](https://www.joeware.net/freetools/tools/admod/index.htm)
   * Command-line tool for modifying AD Objects. Predates PowerShell.
   * This will trip most AV/EDR solutions as the bad guys are using it because it is so good. That is why it isn't starred.
* ✨ AsBuiltReport.Microsoft.AD
   * https://github.com/AsBuiltReport
   * This tool scans your directory and does tons of documentation for you. Also generates drawings of the environments to help with documentation.
     * ❔The drawings do not scale well with large environments.   
   * ❔This may trigger EDR/XDR auditing as it asked for a lot of information. This has not been verified yet though. 
* Delinea (formerly Thycotic) Weak Password Finder 
   * [https://delinea.com/resources/weak-password-finder-tool-active-directory](https://delinea.com/resources/weak-password-finder-tool-active-directory)
* ✨Lithnet Access Manager
   * [https://github.com/lithnet/access-manager](https://github.com/lithnet/access-manager)
   * Allows for some LAPS/RapidLAPS administration.
   * The free version is limited on JIT roles but effectively as fully featured as the paid.
* Cayosoft Guardian
   * [https://www.cayosoft.com/products/guardian/](https://www.cayosoft.com/products/guardian/)
   * [https://www.cayosoft.com/wp-content/uploads/cayosoft-resources/CayosoftInstaller.exe](https://www.cayosoft.com/wp-content/uploads/cayosoft-resources/CayosoftInstaller.exe)
   * Includes their Administrator tool as well. The Guardian product is an okay Active Directory change montioring solution in the freeware mode. The app leaves a lot of features off the table in trial/freeware mode.
   * The Administrator tool is also included but is a pass from my analysis. Perhaps the paid version is useful, but the free one doesn't really do much useful and isn't something I think worth recommending.
* NetCease Module to help remediate Net Session Enumeration 
   * [https://github.com/p0w3rsh3ll/NetCease](https://github.com/p0w3rsh3ll/NetCease)
* SpecOps Password Scanner  - 
   * [https://specopssoft.com/lp/uk/free-active-directory-password-audit/](https://specopssoft.com/lp/uk/free-active-directory-password-audit/)
   * **MOD NOTE:** Used once, not a big fan of dumping passwords.
* PowerPUG - Tool to help with tranisitiong to using Protected Users
   * [https://github.com/jakehildreth/PowerPUG](https://github.com/jakehildreth/PowerPUG)
* 💥 ADRecon - Extracts and combines various artifacts out of AD.
   * [https://github.com/adrecon/ADRecon](https://github.com/adrecon/ADRecon)
* myADMonitor - Open-source AD change tracking tool
   * [https://github.com/mihemihe/myADMonitor](https://github.com/mihemihe/myADMonitor)
   * **MOD NOTE:** Not something meant to be run for a long time, run it for awhile and turn it off. 
* ManagedEsent - Tool for accessing the esent.dll which is the tool that drives the NTDS.DIT
   * [https://github.com/microsoft/ManagedEsent](https://github.com/microsoft/ManagedEsent)
* ❔ Export-ActiveDirectoryVisioMap
   * [https://github.com/KSchu26/Export-ActiveDirectoryVisioMap](https://github.com/KSchu26/Export-ActiveDirectoryVisioMap)
* ❔ Audit Test Automation - Not strictly for AD. Gains a comprehensive review of environments hardening against various guidelines.
   * [https://github.com/fbprogmbh/Audit-Test-Automation](https://github.com/fbprogmbh/Audit-Test-Automation)
* ❔ ADTimeline - Generates a timeline based on AD replication data of for objects of interest.
   * [https://github.com/ANSSI-FR/ADTimeline](https://github.com/ANSSI-FR/ADTimeline)
* ❔ CJWDEV Tools - Various tools
   * [https://www.cjwdev.com/Software.html](https://www.cjwdev.com/Software.html)
* ❔ SITG Compliant Domain Prep
   * [https://github.com/simeononsecurity/STIG-Compliant-Domain-Prep](https://github.com/simeononsecurity/STIG-Compliant-Domain-Prep)
* ❔ Netwrix Tools - There are some issues some of the mods have with their business model and how they farm for emails with free tools.
   * **MOD NOTE -** Netwrix's business model leaves a lot to be desired and they really like to hound people. These are still useful tools but be warned, they'll bug you.
   * ❔Netwrix Lockout Examiner - https://www.netwrix.com/account_lockout_examiner.html
   * ❔Netwrix Inactive User Tracker - [https://www.netwrix.com/netwrix\_inactive\_user\_tracker.html](https://www.netwrix.com/netwrix_inactive_user_tracker.html)
   * ❔Netwrix Effective Permissions Reporting - https://www.netwrix.com/netwrix_effective_permissions_reporting_tool.html
   * ❔Netwrix Password Expiration Notifier - [https://www.netwrix.com/netwrix\_password\_expiration\_notifier.html](https://www.netwrix.com/netwrix_password_expiration_notifier.html)
* IS Decisions Tools - Similar story to Netwrix. Some decent tools that are used to farm for emails to spam.
   * ❔File Audit - [https://www.isdecisions.com/products/fileaudit/](https://www.isdecisions.com/products/fileaudit/)
   * ❔User Lock - [https://www.isdecisions.com/products/userlock/](https://www.isdecisions.com/products/userlock/)
 * ❔Restore from IFM (RIFM) 
   * https://github.com/LDAPAngel/RIFM
   * Tool that builds off of the DSInternals tools to aid in restoring AD from IFM.
 * ❔HeathAD - AD Health Monitoring Tool (TBD)
   * https://dakhama-mehdi.github.io/ADhealth/Example/HealthAD.html

# Password Filters

>These tools can be used to create password filters that can screen passwords against block lists or extra criteria beyond AD's general password policy.

* ✨PassFiltEx (Ryan Ries) - A simple password filter for AD that can block blacklisted passwords and character sequences. Similar to Entra Password Protection.
   * [https://github.com/ryanries/PassFiltEx](https://github.com/ryanries/PassFiltEx)
* ✨Lithnet Password Protection
   * [https://github.com/lithnet/ad-password-protection](https://github.com/lithnet/ad-password-protection)
   * A really good altnerative to other tools. (not starred because I haven't completed my testing)

# In-Built Microsoft Tools (On-Prem)

* Netlogon Debugging
* [https://learn.microsoft.com/en-us/troubleshoot/windows-client/windows-security/enable-debug-logging-netlogon-service](https://learn.microsoft.com/en-us/troubleshoot/windows-client/windows-security/enable-debug-logging-netlogon-service)
   * Generates netlogon debugging events. Useful for troubleshooting DC Locator, some DNS registration stuff, and a host of other things.
   * Enabled via nltest or via registry. Log size can be adjusted via registry.
   * Make sure and disable when done.
* Active Directory Debugging 
   * [https://learn.microsoft.com/en-us/troubleshoot/windows-server/active-directory/configure-ad-and-lds-event-logging](https://learn.microsoft.com/en-us/troubleshoot/windows-server/active-directory/configure-ad-and-lds-event-logging)
   * Can be configured to stack trace level reporting on various components of AD DS/AD LDS.
   * **DO NOT LEAVE THIS ON FOR A LONG TIME**. It will fill up your logs fast.
* Kerberos Event Logging
   * [https://learn.microsoft.com/en-us/troubleshoot/windows-server/active-directory/enable-kerberos-event-logging](https://learn.microsoft.com/en-us/troubleshoot/windows-server/active-directory/enable-kerberos-event-logging)
   * Not to be confused with Audit Policies in GPO.
   * Used to do some high-level Kerberos event logging.

# Lab Tools

* AutomatedLab - AWESOME for deploying labs - [https://github.com/AutomatedLab/AutomatedLab](https://github.com/AutomatedLab/AutomatedLab)
* GameOfAD - vulnerable AD environment - [https://github.com/Orange-Cyberdefense/GOAD](https://github.com/Orange-Cyberdefense/GOAD)
* LUDUS - [https://docs.ludus.cloud/docs/intro](https://docs.ludus.cloud/docs/intro) 
   * Enables a quick build of several kinds of vuln testing labs. Allows for a quick-lab of the GOAD content and some others.
   * **MOD NOTE -** This is a neat tool but requires A LOT to get it up and running
* VulnerableAD - perfect for creating a vulnerable AD environment - [https://github.com/WazeHell/vulnerable-AD](https://github.com/WazeHell/vulnerable-AD)

# CHANGE LOG
* Updated 2024-04 - Included more tools from reddit and from issues. 
* Created 2025-01

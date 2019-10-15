# PesterInfrastructureTests - PowerShell Module

*PesterInfrastructureTests* is PowerShell module allowing to test Active Directory (for now) in fast and efficient way. You can run it in 2 ways as described below. Depending on how you like to approach things you can either copy code or simply install it from PowerShellGallery. I prefer 2nd way so I can update this code in one place and then simply redeploy everywhere with *Update-Module*

**PesterInfrastructureTests** have been replaced by [Testimo](https://github.com/EvotecIT/Testimo) and this project has beeen **deprecated**. 

## Copy code Public Directory

Simply copy code from *Public\ActiveDirectory.ps1* and run it as you like.

## Module from PowerShellGallery way

```powershell
Install-Module PesterInfrastructureTests -Force -SkipPublisherCheck
#Update-Module PesterInfrastructureTests -Force # You can use this line to update the module later on
Test-ADPester
```

## Example output

![Pester AD Example](https://evotec.xyz/wp-content/uploads/2018/07/ADPester-TheMovie.gif)

```powershell
Describing Domain Controller Infrastructure Test
  [+] Active Directory Forest is available 214ms
  [+] Active Directory Domain is available 74ms

  Context AD2.ad.evotec.xyz Availability
    [+] AD2.ad.evotec.xyz Responds to Ping 553ms
    [+] AD2.ad.evotec.xyz Responds on Port 53 148ms
    [+] AD2.ad.evotec.xyz DNS Service is Running 33ms
    [+] AD2.ad.evotec.xyz ADDS Service is Running 12ms
    [+] AD2.ad.evotec.xyz ADWS Service is Running 20ms
    [+] AD2.ad.evotec.xyz KDC Service is Running 19ms
    [+] AD2.ad.evotec.xyz Netlogon Service is Running 45ms

  Context Replication Status
    [+] AD2.ad.evotec.xyz Last Replication Result is 0 (Success) 361ms

  Context AD1.ad.evotec.xyz Availability
    [+] AD1.ad.evotec.xyz Responds to Ping 226ms
    [+] AD1.ad.evotec.xyz Responds on Port 53 150ms
    [+] AD1.ad.evotec.xyz DNS Service is Running 33ms
    [+] AD1.ad.evotec.xyz ADDS Service is Running 14ms
    [+] AD1.ad.evotec.xyz ADWS Service is Running 44ms
    [+] AD1.ad.evotec.xyz KDC Service is Running 19ms
    [+] AD1.ad.evotec.xyz Netlogon Service is Running 12ms

  Context Replication Status
    [+] AD1.ad.evotec.xyz Last Replication Result is 0 (Success) 335ms

  Context Replication Link Status

    Context Source DSA = AD2

      Context Target DSA = AD1
        [+] DC=ad,DC=evotec,DC=xyz - should have zero replication failures 217ms
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 19ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 36ms
        [+] DC=DomainDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 13ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 33ms
        [+] DC=ad,DC=evotec,DC=pl - should have zero replication failures 12ms

      Context Target DSA = ADPREVIEW2019
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 45ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 28ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 12ms
        [+] DC=ad,DC=evotec,DC=xyz - should have zero replication failures 7ms

    Context Source DSA = AD1

      Context Target DSA = AD2
        [+] DC=ad,DC=evotec,DC=xyz - should have zero replication failures 105ms
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 24ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 48ms
        [+] DC=DomainDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 10ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 21ms
        [+] DC=ad,DC=evotec,DC=pl - should have zero replication failures 8ms

    Context Source DSA = ADPREVIEW2019

      Context Target DSA = AD2
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 74ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 19ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 8ms
        [+] DC=ad,DC=evotec,DC=pl - should have zero replication failures 29ms
  [+] Active Directory Domain is available 81ms

  Context ADPreview2019.ad.evotec.pl Availability
    [+] ADPreview2019.ad.evotec.pl Responds to Ping 252ms
    [+] ADPreview2019.ad.evotec.pl Responds on Port 53 154ms
    [+] ADPreview2019.ad.evotec.pl DNS Service is Running 23ms
    [+] ADPreview2019.ad.evotec.pl ADDS Service is Running 50ms
    [+] ADPreview2019.ad.evotec.pl ADWS Service is Running 18ms
    [+] ADPreview2019.ad.evotec.pl KDC Service is Running 31ms
    [+] ADPreview2019.ad.evotec.pl Netlogon Service is Running 38ms

  Context Replication Status
    [+] ADPreview2019.ad.evotec.pl Last Replication Result is 0 (Success) 415ms

  Context Replication Link Status

    Context Source DSA = AD2

      Context Target DSA = AD1
        [+] DC=ad,DC=evotec,DC=xyz - should have zero replication failures 220ms
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 12ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 19ms
        [+] DC=DomainDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 25ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 27ms
        [+] DC=ad,DC=evotec,DC=pl - should have zero replication failures 9ms

      Context Target DSA = ADPREVIEW2019
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 56ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 7ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 9ms
        [+] DC=ad,DC=evotec,DC=xyz - should have zero replication failures 22ms

    Context Source DSA = AD1

      Context Target DSA = AD2
        [+] DC=ad,DC=evotec,DC=xyz - should have zero replication failures 83ms
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 39ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 33ms
        [+] DC=DomainDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 19ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 17ms
        [+] DC=ad,DC=evotec,DC=pl - should have zero replication failures 17ms

    Context Source DSA = ADPREVIEW2019

      Context Target DSA = AD2
        [+] CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 152ms
        [+] CN=Schema,CN=Configuration,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 11ms
        [+] DC=ForestDnsZones,DC=ad,DC=evotec,DC=xyz - should have zero replication failures 23ms
        [+] DC=ad,DC=evotec,DC=pl - should have zero replication failures 31ms

```

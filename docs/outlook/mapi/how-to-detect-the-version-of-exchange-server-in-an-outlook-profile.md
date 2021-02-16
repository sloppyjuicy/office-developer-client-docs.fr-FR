---
title: Détection de la version d’Exchange Server dans un profil Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424447"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Détection de la version d’Exchange Server dans un profil Outlook

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique inclut un exemple de code en C++ qui montre comment utiliser la propriété **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** et la propriété **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** pour obtenir les informations de version du Microsoft Exchange Server à qui le compte actif est connecté. 
  
La  `GetProfileServiceVersion` fonction dans l’exemple de code accepte un profil comme paramètre d’entrée. Selon que la propriété **PR_PROFILE_SERVER_VERSION** et la propriété **PR_PROFILE_SERVER_FULL_VERSION** existent dans le profil donné, la fonction obtient chaque propriété et renvoie les informations de version appropriées en tant que paramètres de sortie. 
  
`GetProfileServiceVersion` appelle **[d’abord la fonction MAPIAdminProfiles pour](mapiadminprofiles.md)** créer un objet d’administration de profil. Il utilise ensuite l’objet d’administration de profil pour appeler **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** pour obtenir un objet d’administration de service de message. À l’aide de l’objet d’administration du service de message, il appelle **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** pour obtenir une section du profil actuel, puis appelle **[HrGetOneProp](hrgetoneprop.md)** pour vérifier si chacune des deux propriétés existe dans cette section du profil et, si c’est le cas, définit les informations de version dans les paramètres de sortie appropriés. 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
    TZDEFINITION tzDef = {0}; 
    TZRULE* lpRules = NULL; 
    LPBYTE lpPtr = lpbDef; 
    WORD cchKeyName = NULL; 
    WCHAR* szKeyName = NULL; 
    WORD i = 0; 
 
    BYTE bMajorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
    BYTE bMinorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
 
    // We only understand TZ_BIN_VERSION_MAJOR 
    if (TZ_BIN_VERSION_MAJOR != bMajorVersion) return NULL; 
 
    // We only understand if &gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```



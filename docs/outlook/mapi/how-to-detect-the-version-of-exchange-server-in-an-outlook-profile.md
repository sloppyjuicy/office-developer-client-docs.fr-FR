---
title: Détecter la version d’Exchange Server dans un profil Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: b6c1482554cfb1e756266eb31f992b81bc34bb51
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575895"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Détecter la version d’Exchange Server dans un profil Outlook

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique inclut un exemple de code en langage C++ qui montre comment utiliser la propriété **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** et la propriété **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** pour obtenir des informations de version de Microsoft Exchange Server qui est le compte actif connecté à. 
  
Le `GetProfileServiceVersion` fonction dans l’exemple de code accepte un profil comme paramètre d’entrée. Selon si la propriété **PR_PROFILE_SERVER_VERSION** et la propriété **PR_PROFILE_SERVER_FULL_VERSION** existent dans le profil donné, la fonction obtient chaque propriété et retourne les informations de la version appropriée en sortie paramètres. 
  
`GetProfileServiceVersion`appelle d’abord la fonction **[MAPIAdminProfiles](mapiadminprofiles.md)** pour créer un objet d’administration de profil. Il utilise ensuite l’objet d’administration de profil à appeler **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** pour obtenir un objet de l’administration de service de message. À l’aide de l’objet de l’administration du service de message, il appelle **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** pour obtenir une section du profil actuel, puis appelle **[HrGetOneProp](hrgetoneprop.md)** pour vérifier si chacun des deux propriétés existe dans cette section de la profil et si c’est le cas, définit les informations de version dans les paramètres de sortie approprié. 
  
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



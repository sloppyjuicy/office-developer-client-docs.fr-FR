---
title: Obtenir un message de contact donné une entrée de carnet d’adresses contacts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Dernière modification : 13 août 2013'
ms.openlocfilehash: 472b5847053c0a18026c76b8055a26551331d8dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564541"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Obtenir un message de contact donné une entrée de carnet d’adresses contacts

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple en langage C++, `HrOpenContact`, qui montre comment utiliser la structure [CONTAB_ENTRYID](contab_entryid.md) qui identifie une entrée dans un carnet d’adresses de Contacts pour obtenir le message MAPI Contact associé. 
  
`HrOpenContact`présente les paramètres suivants : 
  
-  *lpSession* est un paramètre d’entrée représentant la session active. **LPMAPISESSION** est défini dans le mapix.h de fichier d’en-tête MAPI comme un pointeur vers [IMAPISession : IUnknown](imapisessioniunknown.md).
    
-  *cbEntryID* est un paramètre d’entrée représentant la taille de l’identificateur d’entrée associé *lpEntryID* . 
    
-  *lpEntryID* est un paramètre d’entrée qui représente un pointeur vers l’identificateur d’entrée d’une entrée dans un carnet d’adresses de contacts. 
    
-  *ulFlags* est un paramètre d’entrée qui représente un masque de bits contenant des indicateurs d’accès objet au message MAPI Contact. 
    
-  *lpContactMessage* est un paramètre de sortie qui représente un pointeur vers le message MAPI Contact. 
    
Pour ouvrir le message MAPI Contact sous-jacent, `HrOpenContact` affecte *lpEntryID* vers un pointeur vers **CONTAB_ENTRYID**. Il appelle ensuite [IMAPISession::OpenEntry](imapisession-openentry.md) pour obtenir le message MAPI Contact, en passant en tant que paramètres, les champs *cbeid* et *abeid* de l’entrée dans le carnet d’adresses de Contacts qui identifient respectivement la taille de l’identificateur d’entrée et la identificateur d’entrée du message MAPI Contact. 
  
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

## <a name="see-also"></a>Voir aussi

- [IMAPISession::OpenEntry](imapisession-openentry.md)


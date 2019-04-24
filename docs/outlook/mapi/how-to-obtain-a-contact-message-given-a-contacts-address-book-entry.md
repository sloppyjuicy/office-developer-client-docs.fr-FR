---
title: Obtenir un message de contact à partir d'une entrée de carnet d'adresses de contacts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Dernière modification: 13 août 2013'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345954"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="9dae1-103">Obtenir un message de contact à partir d'une entrée de carnet d'adresses de contacts</span><span class="sxs-lookup"><span data-stu-id="9dae1-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="9dae1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dae1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dae1-105">Cette rubrique contient un exemple en C++, `HrOpenContact`qui montre comment utiliser la structure [CONTAB_ENTRYID](contab_entryid.md) qui identifie une entrée dans un carnet d'adresses de contacts pour obtenir le message de contact MAPI associé.</span><span class="sxs-lookup"><span data-stu-id="9dae1-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="9dae1-106">`HrOpenContact`possède les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="9dae1-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="9dae1-107">*lpSession* est un paramètre d'entrée représentant la session en cours.</span><span class="sxs-lookup"><span data-stu-id="9dae1-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="9dae1-108">**LPMAPISESSION** est défini dans le fichier d'en-tête MAPI mapix. h en tant que pointeur vers [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9dae1-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="9dae1-109">*cbEntryID* est un paramètre d'entrée représentant la taille de l'identificateur d'entrée associé à *lpEntryID* .</span><span class="sxs-lookup"><span data-stu-id="9dae1-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="9dae1-110">*lpEntryID* est un paramètre d'entrée représentant un pointeur vers l'identificateur d'entrée d'une entrée dans un carnet d'adresses de contacts.</span><span class="sxs-lookup"><span data-stu-id="9dae1-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="9dae1-111">*ulFlags* est un paramètre d'entrée représentant un masque de masque contenant des indicateurs d'accès aux objets pour le message de contact MAPI.</span><span class="sxs-lookup"><span data-stu-id="9dae1-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="9dae1-112">*lpContactMessage* est un paramètre de sortie qui représente un pointeur vers le message de contact MAPI.</span><span class="sxs-lookup"><span data-stu-id="9dae1-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="9dae1-113">Pour ouvrir le message de contact MAPI sous `HrOpenContact` -jacent, convertit d'abord *lpEntryID* en pointeur vers **CONTAB_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="9dae1-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="9dae1-114">Il appelle ensuite [IMAPISession:: OpenEntry](imapisession-openentry.md) pour obtenir le message de contact MAPI, en transmettant en tant que paramètres les champs *cbeid* et *Abeid* de l'entrée dans le carnet d'adresses de contacts qui identifie respectivement la taille de l'identificateur d'entrée et le identificateur d'entrée du message de contact MAPI.</span><span class="sxs-lookup"><span data-stu-id="9dae1-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9dae1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dae1-115">See also</span></span>

- [<span data-ttu-id="9dae1-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="9dae1-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)


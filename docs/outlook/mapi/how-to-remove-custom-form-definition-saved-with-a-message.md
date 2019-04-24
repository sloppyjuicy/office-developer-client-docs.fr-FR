---
title: Suppression de la définition de formulaire personnalisé enregistrée avec un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345933"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="a0ae2-103">Suppression de la définition de formulaire personnalisé enregistrée avec un message</span><span class="sxs-lookup"><span data-stu-id="a0ae2-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="a0ae2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0ae2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0ae2-105">Cette rubrique présente un exemple de code en C++ qui convertit un message qui a été enregistré avec une définition de formulaire personnalisée en un message normal sans la définition du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="a0ae2-106">Dans Microsoft Outlook 2010 ou Microsoft Outlook 2013, vous pouvez partager des formulaires contenant des pages de formulaire personnalisées en les publiant dans une bibliothèque de formulaires ou en enregistrant la définition de formulaire correspondante avec un message.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="a0ae2-107">Un formulaire personnalisé enregistré avec un message est communément appelé «formulaire unique», étant donné que le formulaire est partagé uniquement pour afficher ce message spécifique en tant qu'instance isolée.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="a0ae2-108">Vous effectuez généralement cette opération lorsque le formulaire n'est pas publié dans une bibliothèque de formulaires, mais que vous souhaitez que le destinataire utilise le formulaire personnalisé lors de l'ouverture de l'élément.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="a0ae2-109">Vous pouvez spécifier un formulaire en une seule fois dans le concepteur de formulaires, en activant la case à cocher **Envoyer la définition du formulaire avec l'élément** sur la page **Propriétés** du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="a0ae2-110">Les formulaires contenant des pages de formulaire peuvent être personnalisés avec du code Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a0ae2-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="a0ae2-111">Les messages enregistrés avec des définitions de formulaire sont généralement plus volumineux.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="a0ae2-112">Pour des raisons de sécurité et de stockage, Outlook 2010 et Outlook 2013 ignorent les définitions de formulaire enregistrées avec n'importe quel élément.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="a0ae2-113">Pour convertir un message enregistré avec une définition de formulaire personnalisé en un message sans, vous devez supprimer quatre propriétés nommées:</span><span class="sxs-lookup"><span data-stu-id="a0ae2-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="a0ae2-114">Propri�t� canonique PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="a0ae2-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="a0ae2-115">Propri�t� canonique PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="a0ae2-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="a0ae2-116">Propri�t� canonique PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="a0ae2-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="a0ae2-117">Propri�t� canonique PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="a0ae2-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="a0ae2-118">En outre, vous devez également supprimer la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) qui contient les définitions des propriétés personnalisées enregistrées avec ce message.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="a0ae2-119">L'un des effets secondaires de la suppression de cette propriété est que les modèles d'objet Outlook 2010 ou Outlook 2013 et l'interface utilisateur d'Outlook 2010 ou Outlook 2013 ne pourront plus accéder aux propriétés de l'utilisateur qui ont été définies sur le message.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="a0ae2-120">Vous pouvez toujours accéder à ces propriétés et à leurs valeurs via MAPI.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="a0ae2-121">Notez que si vous ne supprimez pas cette propriété et que le message est enregistré avec une autre définition de formulaire, la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) est partiellement remplacée par les nouvelles données et l'intégrité des données n'est pas garantie.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="a0ae2-122">Si vous supprimez la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), vous devez également supprimer l'indicateur **INSP_PROPDEFINITION** de la [propriété canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="a0ae2-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="a0ae2-123">La fonction suivante, `RemoveOneOff`, accepte comme paramètres d'entrée un pointeur vers un message et un indicateur s'il faut supprimer la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="a0ae2-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="a0ae2-124">À l'aide du pointeur de message, il appelle [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir les identificateurs de propriété appropriés, puis appelle [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) pour supprimer les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="a0ae2-125">Il appelle également [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la [propriété canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md) et efface l' **indicateur\_INSP ONEOFFFLAGS** et l'indicateur **INSP_PROPDEFINITION** en fonction des besoins de cette propriété, afin qu'Outlook 2010 et Outlook 2013 ne recherche pas les propriétés nommées qui ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="a0ae2-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
```cpp
ULONG aulOneOffIDs[] = {dispidFormStorage,  
    dispidPageDirStream, 
    dispidFormPropStream, 
    dispidScriptStream, 
    dispidPropDefStream, // dispidPropDefStream must remain next to last in list 
    dispidCustomFlag};   // dispidCustomFlag must remain last in list 
 
#define ulNumOneOffIDs (sizeof(aulOneOffIDs)/sizeof(aulOneOffIDs[0])) 
 
HRESULT RemoveOneOff(LPMESSAGE lpMessage, BOOL bRemovePropDef) 
{ 
    if (!lpMessage) return MAPI_E_INVALID_PARAMETER; 
     
    HRESULT hRes = S_OK; 
    MAPINAMEID  rgnmid[ulNumOneOffIDs]; 
    LPMAPINAMEID rgpnmid[ulNumOneOffIDs]; 
    LPSPropTagArray lpTags = NULL; 
 
    ULONG i = 0; 
    for (i = 0 ; i < ulNumOneOffIDs ; i++) 
    { 
        rgnmid[i].lpguid = (LPGUID)&PSETID_Common; 
        rgnmid[i].ulKind = MNID_ID; 
        rgnmid[i].Kind.lID = aulOneOffIDs[i]; 
        rgpnmid[i] = &rgnmid[i]; 
    } 
   
    hRes = lpMessage->GetIDsFromNames( 
        ulNumOneOffIDs, 
        rgpnmid, 
        0, 
        &lpTags); 
    if (lpTags) 
    { 
        // The last prop is the flag value  
        // to be updated, don't count it 
        lpTags->cValues = ulNumOneOffIDs-1; 
 
        // If the prop def stream is not to be removed, don't count it 
        if (!bRemovePropDef) 
        { 
          lpTags->cValues = lpTags->cValues-1; 
        } 
 
        hRes = lpMessage->DeleteProps( 
            lpTags, 
            0); 
        if (SUCCEEDED(hRes)) 
        { 
            SPropTagArray pTag = {0}; 
            ULONG cProp = 0; 
            LPSPropValue lpCustomFlag = NULL; 
 
            // Grab dispidCustomFlag, the last tag in the array 
            pTag.cValues = 1; 
            pTag.aulPropTag[0] = CHANGE_PROP_TYPE( 
                lpTags->aulPropTag[ulNumOneOffIDs-1], 
                PT_LONG); 
 
            hRes = lpMessage->GetProps( 
                &pTag, 
                fMapiUnicode, 
                &cProp, 
                &lpCustomFlag); 
            if (SUCCEEDED(hRes) &&  
                1 == cProp && lpCustomFlag &&  
                PT_LONG == PROP_TYPE(lpCustomFlag->ulPropTag)) 
            { 
                // Clear the INSP_ONEOFFFLAGS bits so Outlook  
                // doesn't look for the props that have been deleted 
                lpCustomFlag->Value.l =  
                    lpCustomFlag->Value.l & ~(INSP_ONEOFFFLAGS); 
                if (bRemovePropDef) 
                { 
                    lpCustomFlag->Value.l =  
                        lpCustomFlag->Value.l & ~(INSP_PROPDEFINITION); 
                } 
                hRes = lpMessage->SetProps( 
                    1, 
                    lpCustomFlag, 
                    NULL); 
             } 
 
             hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE); 
         } 
    } 
    MAPIFreeBuffer(lpTags); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="a0ae2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0ae2-126">See also</span></span>

- [<span data-ttu-id="a0ae2-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a0ae2-127">MAPI Constants</span></span>](mapi-constants.md)


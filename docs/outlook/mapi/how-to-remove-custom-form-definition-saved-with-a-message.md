---
title: Suppression de la définition de formulaire personnalisé enregistrée avec un message
description: Cet article explique comment convertir un message enregistré avec une définition de formulaire personnalisée en message normal sans définition de formulaire.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
ms.openlocfilehash: a86d84b2252eac68b6156e0edddbf1eec0bd8532
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817913"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Suppression de la définition de formulaire personnalisé enregistrée avec un message
  
**S’applique à** : Outlook 2013 | Outlook 2016
  
Cette rubrique montre un exemple de code en C++ qui convertit un message enregistré avec une définition de formulaire personnalisée en message normal sans définition de formulaire.
  
Dans Microsoft Outlook 2010 ou Microsoft Outlook 2013, vous pouvez partager des formulaires contenant des pages de formulaire personnalisées en les publiant dans une bibliothèque de formulaires ou en enregistrant la définition de formulaire correspondante avec un message. Un formulaire personnalisé enregistré avec un message est communément appelé « formulaire unique », car le formulaire est partagé uniquement pour afficher ce message spécifique en tant qu’instance unique. Vous effectuez généralement cette opération lorsque le formulaire n’est pas publié dans une bibliothèque de formulaires, mais que vous souhaitez que le destinataire utilise le formulaire personnalisé lors de l’ouverture de l’élément. Vous pouvez spécifier qu’un formulaire est unique dans le Concepteur de formulaires, en sélectionnant la **définition de formulaire Envoyer avec** la case à cocher d’élément dans la page **Propriétés** du formulaire.
  
Les formulaires contenant des pages de formulaire peuvent être personnalisés avec du code dans Visual Basic Scripting Edition (VBScript). Les messages enregistrés avec des définitions de formulaire sont généralement plus volumineux. Pour des raisons de sécurité et de stockage, Outlook 2010 et Outlook 2013 ignorent les définitions de formulaire enregistrées avec n’importe quel élément.
  
Pour convertir un message enregistré avec une définition de formulaire personnalisée en un message sans, vous devez supprimer quatre propriétés nommées :
  
- [Propri�t� canonique PidLidFormStorage](pidlidformstorage-canonical-property.md)

- [Propri�t� canonique PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)

- [Propri�t� canonique PidLidFormPropStream](pidlidformpropstream-canonical-property.md)

- [Propri�t� canonique PidLidScriptStream](pidlidscriptstream-canonical-property.md)

En outre, vous devez également supprimer la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) qui contient les définitions des propriétés personnalisées enregistrées avec ce message. La suppression de cette propriété a pour effet secondaire que les modèles objet Outlook 2010 ou Outlook 2013 et l’interface utilisateur Outlook 2010 ou Outlook 2013 ne pourront plus accéder aux propriétés utilisateur définies sur le message. Vous pouvez toujours accéder à ces propriétés et à leurs valeurs via MAPI. Notez que si vous ne supprimez pas cette propriété et que le message est enregistré avec une autre définition de formulaire, la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) est partiellement remplacée par de nouvelles données et l’intégrité des données n’est pas garantie.
  
Si vous supprimez la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), vous devez également supprimer l’indicateur **INSP_PROPDEFINITION** de la [propriété canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md).
  
La fonction suivante, `RemoveOneOff`accepte en tant que paramètres d’entrée un pointeur vers un message et un indicateur indiquant s’il faut supprimer la [propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). À l’aide du pointeur de message, il appelle [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir les identificateurs de propriété appropriés, puis appelle [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) pour supprimer les propriétés nommées. Il appelle également [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la [propriété canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md) et efface l’indicateur **INSP\_ONEOFFFLAGS** et **l’indicateur INSP_PROPDEFINITION** comme il convient à partir de cette propriété, afin que Outlook 2010 et Outlook 2013 ne recherchent pas les propriétés nommées qui ont été supprimées.
  
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

## <a name="see-also"></a>Voir aussi

- [Constantes MAPI](mapi-constants.md)

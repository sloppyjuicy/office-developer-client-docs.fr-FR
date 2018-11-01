---
title: Suppression de la définition de formulaire personnalisé enregistrée avec un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: 4b12824542a1408a364452eb6587122ec66412d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594452"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Suppression de la définition de formulaire personnalisé enregistrée avec un message
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente un exemple de code en langage C++ qui convertit un message qui a été enregistré avec une définition de formulaire personnalisé à un message régulière sans la définition du formulaire.
  
Dans Microsoft Outlook 2010 ou Microsoft Outlook 2013, vous pouvez partager les formulaires contenant des pages de formulaire personnalisées en publiant sur une bibliothèque de formulaires ou l’enregistrement de la définition de formulaire correspondant à un message. Un formulaire personnalisé enregistré avec un message est généralement désigné comme « uniques », dans la mesure où le formulaire est partagé uniquement pour l’affichage de ce message spécifique comme une instance unique. Cela s’effectue généralement lorsque le formulaire n’est pas publié dans une bibliothèque de formulaires, mais que vous souhaitez que le destinataire à utiliser le formulaire personnalisé lors de l’ouverture de l’élément. Vous pouvez spécifier qu'un formulaire est One-Off dans le Concepteur de formulaires en activant la case à cocher **Envoyer la définition du formulaire avec l’élément** dans la page **Propriétés** du formulaire. 
  
Les formulaires contenant des pages de formulaire peuvent être personnalisés avec du code en Visual Basic Scripting Edition (VBScript). Les messages qui sont enregistrés avec les définitions de formulaire sont généralement une plus grand taille. Pour des raisons de stockage et de sécurité, Outlook 2010 et Outlook 2013 ignore les définitions de formulaire enregistrées avec n’importe quel élément.
  
Pour convertir un message est enregistré dans une définition de formulaire personnalisé à l’autre sans, vous devez supprimer les quatre propriétés nommées :
  
- [Propriété canonique PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propriété canonique PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propriété canonique PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propriété canonique PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
En outre, vous devez également supprimer la [Propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) qui contient les définitions de propriétés personnalisées enregistrées avec ce message. Un effet secondaire de la suppression de cette propriété est que les modèles d’objet Outlook 2010 ou Outlook 2013 et l’interface utilisateur Outlook 2010 ou Outlook 2013 ne sera plus en mesure d’accéder aux propriétés utilisateur ont été définies sur le message. Vous ne pouvez toujours accéder à ces propriétés et leurs valeurs par le biais de MAPI. Notez que si vous ne supprimez pas cette propriété et le message est enregistré avec une autre définition du formulaire, la [Propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) est partiellement remplacé avec les nouvelles données et l’intégrité des données ne sont pas garantie. 
  
Si vous supprimez la [Propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), vous devez également supprimer l’indicateur **INSP_PROPDEFINITION** à partir de la [Propriété canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md).
  
La fonction suivante, `RemoveOneOff`, accepte comme paramètres d’entrée un pointeur vers un message et un indicateur s’il faut supprimer la [Propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). À l’aide du pointeur de message, il appelle [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir les identificateurs de propriété appropriée et appelle ensuite [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) pour supprimer les propriétés nommées. Il appelle [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la [Propriété canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md) et efface également la **INSP\_ONEOFFFLAGS** indicateur et **INSP_PROPDEFINITION** marquer comme il convient à partir de cette propriété, ainsi que Outlook 2010 et Outlook 2013 ne recherche pas de ces propriétés nommées qui ont été supprimées. 
  
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


---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436208"
---
# <a name="rtfsync"></a>RTFSync

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Garantit que le texte du message au format RTF (Rich Text Format) correspond à la version en texte brut. Il est nécessaire d'appeler cette fonction avant de lire la version RTF et après avoir modifié la version RTF. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes compatibles RTF et fournisseurs de banques de messages  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Paramètres

_lpMessage_
  
> dans Pointeur vers le message à mettre à jour.
    
_ulFlags_
  
> dans Masque de des indicateurs utilisé pour indiquer que la version au format RTF ou texte brut du message a changé. Les indicateurs suivants peuvent être définis:
    
  - RTF_SYNC_BODY_CHANGED: la version en texte brut du message a changé.
      
  - RTF_SYNC_RTF_CHANGED: la version RTF du message a changé.
    
  Tous les autres bits dans le paramètre _ulFlags_ sont réservés à une utilisation ultérieure. 
    
_lpfMessageUpdated_
  
> remarquer Pointeur vers une variable qui indique s'il existe un message mis à jour. TRUE s'il existe un message mis à jour, FALSe dans le cas contraire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquANTE ou a la valeur false, avant de lire la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la fonction **RTFSync** doit être appelée avec le RTF_SYNC_BODY_ Indicateur modifié. 
  
Si l'indicateur STORE_RTF_OK n'est pas défini dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), cette fonction doit être appelée avec l'indicateur RTF_SYNC_RTF_CHANGED défini après la modification de **PR_RTF_COMPRESSED**. 
  
Si **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ont été modifiés, la fonction **RTFSync** doit être appelée avec les deux indicateurs définis. 
  
Si la valeur du paramètre _lpfMessageUpdated_ est définie sur true, la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) doit être appelée pour le message. Si **SaveChanges** n'est pas appelé, les modifications ne seront pas enregistrées dans le message. 
  
Les fournisseurs de banques de messages peuvent utiliser **RTFSync** pour synchroniser les propriétés **PR_BODY** et **PR_RTF_COMPRESSED** . 
  
Pour plus d'informations, consultez la rubrique [prise en charge de texte RTF pour les fournisseurs de banque de messages](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Voir aussi

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)


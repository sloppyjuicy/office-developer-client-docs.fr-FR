---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: S’assure que le texte du message RTF correspond à la version en texte simple. Appelez cette fonction avant de lire la version RTF et après avoir modifié la version RTF.
ms.openlocfilehash: ce64b47886618e7f96e875d6cce3cada4aaba110
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406287"
---
# <a name="rtfsync"></a>RTFSync

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet de s’assurer que le texte du message rtf (Rich Text Format) correspond à la version en texte simple. Il est nécessaire d’appeler cette fonction avant de lire la version RTF et après avoir modifié la version RTF. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes rtF et fournisseurs de magasins de messages  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Paramètres

_lpMessage_
  
> [in] Pointeur vers le message à mettre à jour.
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour indiquer que la version RTF ou en texte simple du message a changé. Les indicateurs suivants peuvent être définies :
    
  - RTF_SYNC_BODY_CHANGED : la version en texte simple du message a changé.
      
  - RTF_SYNC_RTF_CHANGED : la version RTF du message a changé.
    
  Tous les autres bits du _paramètre ulFlags_ sont réservés pour une utilisation ultérieure. 
    
_lpfMessageUpdated_
  
> [out] Pointeur vers une variable indiquant s’il existe un message mis à jour. TRUE s’il existe un message mis à jour, FALSE dans le cas contraire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquante ou a la valeur FALSE, avant de lire la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la fonction **RTFSync** doit être appelée avec l’indicateur RTF_SYNC_BODY_CHANGED. 
  
Si l’indicateur STORE_RTF_OK n’est pas définie dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), cette fonction doit être appelée avec l’indicateur RTF_SYNC_RTF_CHANGED définie après la modification **PR_RTF_COMPRESSED.** 
  
Si les **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ont été modifiés, la fonction **RTFSync** doit être appelée avec les deux indicateurs. 
  
Si la valeur du paramètre  _lpfMessageUpdated_ est définie sur TRUE, la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) doit être appelée pour le message. Si **SaveChanges n’est** pas appelé, les modifications ne seront pas enregistrées dans le message. 
  
Les fournisseurs de magasins de messages peuvent utiliser **RTFSync** pour maintenir les propriétés **PR_BODY et** **PR_RTF_COMPRESSED** synchronisées. 
  
Pour plus d’informations, voir [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Voir aussi

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)


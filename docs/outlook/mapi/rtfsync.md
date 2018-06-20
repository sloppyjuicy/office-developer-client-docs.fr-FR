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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787047"
---
# <a name="rtfsync"></a>RTFSync

**S’applique à**: Outlook 
  
Permet de s’assurer que le texte du message RTF (RICH Text Format) correspond à la version en texte brut. Il est nécessaire d’appeler cette fonction avant de lire la version RTF et après avoir modifié la version RTF. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de magasin de message et les applications clientes compatibles RTF  <br/> |
   
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
  
> [in] Masque de bits d’indicateurs utilisés pour indiquer la version du message en texte brut ou RTF a changé. Les indicateurs suivants peuvent être définis :
    
  - RTF_SYNC_BODY_CHANGED : La version en texte brut du message a été modifiée.
      
  - RTF_SYNC_RTF_CHANGED : La version RTF du message a été modifiée.
    
  Tous les autres bits dans le paramètre _ulFlags_ sont réservés pour une utilisation future. 
    
_lpfMessageUpdated_
  
> [out] Pointeur vers une variable qui indique s’il existe un message mis à jour. TRUE si un message mis à jour, FALSE dans le cas contraire.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est introuvable ou est FALSE, avant de lire la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) la fonction **RTFSync** doit être appelée avec le RTF_SYNC_BODY_ MODIFIER l’indicateur. 
  
Si l’indicateur STORE_RTF_OK n’est pas définie dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), cette fonction doit être appelée avec l’indicateur RTF_SYNC_RTF_CHANGED après avoir modifié **PR_RTF_COMPRESSED**. 
  
Si **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ont été modifiés, la fonction **RTFSync** doit être appelée avec les deux indicateurs définis. 
  
Si la valeur du paramètre _lpfMessageUpdated_ est définie sur TRUE, la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) doit être appelée pour le message. Si **SaveChanges** n’est pas appelée, les modifications ne seront pas enregistrées dans le message. 
  
Fournisseurs de magasins message permet de conserver les propriétés **PR_BODY** et **PR_RTF_COMPRESSED** synchronisées **RTFSync** . 
  
Pour plus d’informations, voir [Prise en charge de texte RTF pour les fournisseurs de banque de messages](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Voir aussi

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)


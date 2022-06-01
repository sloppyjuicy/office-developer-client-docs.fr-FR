---
title: IMAPIMessageSiteGetSiteStatus
description: IMAPIMessageSiteGetSiteStatus retourne des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
ms.openlocfilehash: 4471e29ab98f7c202e1aa8ed3d4d0510dae2042d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816842"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Paramètres

 _lpulStatus_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui fournit des informations sur l’état du message. Les indicateurs suivants peuvent être définis :
    
VCSTATUS_COPY 
  
> Le message peut être copié. 
    
VCSTATUS_DELETE 
  
> Le message peut être supprimé.
    
VCSTATUS_DELETE_IS_MOVE 
  
> En cas de suppression, un message est déplacé vers un dossier **Éléments supprimés** dans son magasin de messages au lieu d’être immédiatement supprimé de son magasin de messages. 
    
VCSTATUS_MOVE 
  
> Le message peut être déplacé.
    
VCSTATUS_NEW_MESSAGE 
  
> Un nouveau message peut être créé.
    
VCSTATUS_SAVE 
  
> Le message peut être enregistré.
    
VCSTATUS_SUBMIT 
  
> Le message peut être envoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les objets Form appellent la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir les fonctionnalités de l’objet de site de message pour le message actuel. Les indicateurs retournés dans le paramètre _lpulStatus_ fournissent des informations sur le site de message. En règle générale, un formulaire active ou désactive les commandes de menu, en fonction des informations fournies par les indicateurs sur les fonctionnalités de l’implémentation du site de message. Si un nouveau message est chargé dans un formulaire par la méthode [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou la méthode [IPersistMessage::Load](ipersistmessage-load.md) , les indicateurs d’état doivent être vérifiés. Certains objets de site de messages, en particulier les objets en lecture seule, n’autorisent pas l’enregistrement ou la suppression des messages. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La méthode **IMAPIMessageSite::GetSiteStatus** peut nécessiter que l’application cliente effectue un calcul pour déterminer quelles opérations peuvent ou ne peuvent pas être effectuées sur le message actuel. En règle générale, cela implique d’examiner la ligne d’état du fournisseur du magasin de messages du message actuel ou d’interroger le fournisseur du magasin pour déterminer les actions que l’application cliente peut effectuer à l’aide du magasin de messages. Par exemple, pour déterminer s’il faut renvoyer l’indicateur MAPI_DELETE_IS_MOVE, vérifiez la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) de l’objet de magasin de messages pour voir s’il existe un dossier **Éléments supprimés** dans le magasin de messages. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, consultez [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir l’état du site spécifié. Il peut retourner VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT. |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Propriété canonique PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)


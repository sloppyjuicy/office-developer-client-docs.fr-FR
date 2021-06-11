---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430125"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameters

 _lpulStatus_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui fournit des informations sur l’état du message. Les indicateurs suivants peuvent être définies :
    
VCSTATUS_COPY 
  
> Le message peut être copié. 
    
VCSTATUS_DELETE 
  
> Le message peut être supprimé.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Lorsqu’il est supprimé, un  message est déplacé vers un dossier Éléments supprimés de sa boutique de messages au lieu d’être immédiatement supprimé de sa boutique de messages. 
    
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

Les objets form appellent la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir les fonctionnalités de l’objet de site de message pour le message actuel. Les indicateurs renvoyés dans le  _paramètre lpulStatus_ fournissent des informations sur le site de message. En règle générale, un formulaire active ou désactive les commandes de menu, en fonction des informations fournies par les indicateurs sur les fonctionnalités de l’implémentation du site de message. Si un nouveau message est chargé dans un formulaire par la méthode [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou [IPersistMessage::Load,](ipersistmessage-load.md) les indicateurs d’état doivent être vérifiés. Certains objets de site de message, en particulier les objets en lecture seule, n’autorisent pas l’enregistré ou la suppression des messages. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La **méthode IMAPIMessageSite::GetSiteStatus** peut exiger que l’application cliente effectue un calcul pour déterminer les opérations qui peuvent ou ne peuvent pas être effectuées sur le message actuel. En règle générale, cela implique de regarder la ligne d’état du fournisseur de la boutique de messages du message actuel ou d’interroger le fournisseur de magasin pour déterminer les actions que l’application cliente peut effectuer à l’aide de la boutique de messages. Par exemple, pour déterminer s’il faut renvoyer l’indicateur MAPI_DELETE_IS_MOVE, vérifiez la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) de l’objet de la boutique de messages pour voir s’il existe un dossier Éléments supprimés dans la magasin de messages.  
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir l’état du site spécifié. Elle peut renvoyer VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Propriété canonique PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)


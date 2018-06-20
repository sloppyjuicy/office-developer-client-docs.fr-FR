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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783838"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**S’applique à**: Outlook 
  
Retourne des informations à partir d’un objet de site message sur le message fonctionnalités du site pour le message en cours.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Paramètres

 _lpulStatus_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui fournit des informations sur le statut du message. Les indicateurs suivants peuvent être définis :
    
VCSTATUS_COPY 
  
> Le message peut être copié. 
    
VCSTATUS_DELETE 
  
> Le message peut être supprimé.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Lors de la suppression, un message est déplacé vers le dossier **Éléments supprimés** dans la base de messages au lieu immédiatement supprimé à partir de la base de messages. 
    
VCSTATUS_MOVE 
  
> Le message peut être déplacé.
    
VCSTATUS_NEW_MESSAGE 
  
> Un message peut être créé.
    
VCSTATUS_SAVE 
  
> Le message peut être enregistré.
    
VCSTATUS_SUBMIT 
  
> Le message peut être envoyé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir les fonctionnalités de l’objet de site de message pour le message en cours. Les indicateurs retournés dans le paramètre _lpulStatus_ fournissent des informations sur le site de message. En règle générale, un formulaire active ou désactive les commandes de menu, en fonction des informations que fournissent les indicateurs sur les possibilités de l’implémentation de sites de message. Si un nouveau message est chargé dans un formulaire par la méthode [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou la méthode [IPersistMessage::Load](ipersistmessage-load.md) , les indicateurs d’état doivent être vérifiées. Certains objets du site de message, notamment les objets en lecture seule, ne pas autorisent les messages d’être enregistré ou supprimé. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

La méthode **IMAPIMessageSite::GetSiteStatus** peut nécessiter l’application cliente pour effectuer des calculs pour déterminer les opérations peuvent ou ne peut pas être effectuées sur le message en cours. En règle générale, qui implique la recherche au niveau de la ligne d’état pour le fournisseur de banque de messages du message en cours, ou l’application cliente interroger le fournisseur de banque pour déterminer les actions qui permettre effectuer à l’aide de la banque de messages. Par exemple, pour déterminer s’il faut retourner l’indicateur MAPI_DELETE_IS_MOVE, vérifiez propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) de l’objet de banque de messages pour voir s’il existe un dossier **Éléments supprimés** dans le banque de messages. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
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


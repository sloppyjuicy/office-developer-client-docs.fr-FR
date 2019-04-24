---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309988"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un service de messagerie d'un profil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Paramètres

 _lpuid_
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique pour le service de messagerie à supprimer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de messagerie a été supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** pointé par _lpuid_ ne correspond pas à un service de messagerie existant. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::D eletemsgservice** supprime un service de messagerie d'un profil. **DeleteMsgService** supprime toutes les sections de profil liées au service de messagerie. 
  
 **DeleteMsgService** effectue les étapes suivantes pour supprimer le service de messagerie: 
  
1. Appelle la fonction de point d'entrée du service de messagerie avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE avant la suppression des sections de profil. Cela permet au service d'effectuer des tâches spécifiques aux services. 
    
2. Supprime le service de messagerie.
    
3. Supprime la section de profil du service de messagerie.
    
La fonction de point d'entrée du service de messagerie n'est pas rappelée une fois que le service a été supprimé.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer la structure **MAPIUID** pour le service de messagerie à supprimer, récupérez la colonne de propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de messagerie dans la table de service de message. Pour plus d'informations, reportez-vous à la procédure décrite dans la méthode [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::D eletemsgservice** pour supprimer le service sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


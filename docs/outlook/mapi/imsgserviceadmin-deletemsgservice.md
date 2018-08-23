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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e0d3d669982bee309901f913612ac1fb1622e60a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571142"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Supprime un service de message d’un profil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Paramètres

 _lpuid_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message à supprimer. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le service de message a été supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** désignés par _lpuid_ ne correspond pas à un service de message existant. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::DeleteMsgService** supprime un service de message d’un profil. **DeleteMsgService** supprime toutes les sections profil liées au service de message. 
  
 **DeleteMsgService** effectue les étapes suivantes pour supprimer le service de message : 
  
1. Appelle la fonction de point d’entrée du service de message avec le paramètre _ulContext_ la valeur MSG_SERVICE_DELETE avant que les sections de profil sont supprimées. Cela permet au service exécuter des tâches spécifiques aux services. 
    
2. Supprime le service de message.
    
3. Supprime la section de profil du service de message.
    
Fonction de point d’entrée du service de message n’est pas appelée à nouveau une fois que le service a été supprimé.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour récupérer la structure **MAPIUID** pour le service de message à supprimer, récupérez la colonne de la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table de service de message. Pour plus d’informations, voir la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::DeleteMsgService** pour supprimer le service sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


---
title: IMsgServiceAdminDeleteMsgService
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMsgServiceAdmin DeleteMsgService, qui supprime un service de message d’un profil.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
ms.openlocfilehash: fc1f8d0560d3f9a8e461fe46b18a13385e1d73cf
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828566"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un service de message d’un profil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Paramètres

 _lpuid_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à supprimer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de message a été supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** pointé par  _lpuid_ ne correspond pas à un service de message existant. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::D eleteMsgService** supprime un service de message d’un profil. **DeleteMsgService** supprime toutes les sections de profil liées au service de message. 
  
 **DeleteMsgService** effectue les étapes suivantes pour supprimer le service de message : 
  
1. Appelle la fonction de point d’entrée du service de message avec le paramètre  _ulContext_ défini sur MSG_SERVICE_DELETE avant la suppression des sections de profil. Cela permet au service d’effectuer des tâches spécifiques au service. 
    
2. Supprime le service de message.
    
3. Supprime la section profil du service de message.
    
La fonction de point d’entrée du service de message n’est plus appelée une fois le service supprimé.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer la structure **MAPIUID** du service de message à supprimer, récupérez la colonne de **propriétés PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table du service de messages. Pour plus d’informations, consultez la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::D eleteMsgService** pour supprimer le service sélectionné. |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


---
title: IMsgServiceAdminDeleteMsgService
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 956af277a2966e40887543fd046248efd29d8177
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772006"
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
  
> Le **MAPIUID pointé** par  _lpuid_ ne correspond pas à un service de message existant. 
    
## <a name="remarks"></a>Remarques

La **méthode IMsgServiceAdmin::D eleteMsgService** supprime un service de message d’un profil. **DeleteMsgService** supprime toutes les sections de profil liées au service de message. 
  
 **DeleteMsgService** effectue les étapes suivantes pour supprimer le service de message : 
  
1. Appelle la fonction de point d’entrée du service de message avec le paramètre  _ulContext_ MSG_SERVICE_DELETE avant la suppression des sections de profil. Cela permet au service d’effectuer des tâches spécifiques au service. 
    
2. Supprime le service de message.
    
3. Supprime la section de profil du service de message.
    
La fonction de point d’entrée du service de message n’est pas appelée une fois le service supprimé.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer la structure **MAPIUID** du service de message à supprimer, récupérez la colonne de propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table de service de message. Pour plus d’informations, voir la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise **la méthode IMsgServiceAdmin::D eleteMsgService pour** supprimer le service sélectionné. |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


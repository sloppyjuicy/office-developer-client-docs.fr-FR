---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 368c32374e47dd97dce54980c566ac14f78c75ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620715"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table des services de message, une liste des services de message dans le profil.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Toujours NULL.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau du service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de service de message a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::GetMsgServiceTable** permet d’accéder à la table de service de message, une table que MAPI tient à jour et qui répertorie les services de message actuellement installés dans le profil de session. Pour obtenir la liste complète des colonnes dans le tableau des services de messages, consultez la [table Service de messages.](message-service-tables.md)
  
La table de service de message est statique. Une fois qu’un client a été autorisé à y accéder, les ajouts ou suppressions de service de message suivants ne l’affecteront pas. S’il n’existe aucun service de message dans le profil actuel, **GetMsgServiceTable renvoie** un tableau avec zéro ligne. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::GetMsgServiceTable** pour charger la table des services dans un profil à afficher dans l’affichage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


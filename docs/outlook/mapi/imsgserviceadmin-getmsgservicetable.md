---
title: IMsgServiceAdminGetMsgServiceTable
description: IMsgServiceAdmin GetMsgServiceTable fournit l’accès à la table du service de messages, une liste des services de messages dans le profil.
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
ms.openlocfilehash: 186afe7abdeb148aa3cb43464a9383008b187872
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827750"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à la table du service de messages, une liste des services de messages dans le profil.
  
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
  
> [out] Pointeur vers un pointeur vers la table du service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table du service de message a été retournée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::GetMsgServiceTable** fournit l’accès à la table du service de messages, une table que MAPI gère qui répertorie les services de messages actuellement installés dans le profil de session. Pour obtenir la liste complète des colonnes de la table de service de message, consultez [La table du service de](message-service-tables.md) message.
  
La table du service de message est statique. Une fois qu’un client a reçu l’accès à celui-ci, les ajouts ou suppressions de service de message suivants ne l’affecteront pas. S’il n’existe aucun service de message dans le profil actuel, **GetMsgServiceTable** retourne une table avec zéro ligne. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::GetMsgServiceTable** pour charger la table des services dans un profil à afficher dans la vue. |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


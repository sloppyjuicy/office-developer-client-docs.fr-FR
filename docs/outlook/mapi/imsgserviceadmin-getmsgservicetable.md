---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410475"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l'accès à la table de service de messagerie, une liste des services de messagerie dans le profil.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Toujours NULL.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table de service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de service de message a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin:: GetMsgServiceTable** donne accès à la table des services de messagerie, une table gérée par MAPI, qui répertorie les services de messagerie actuellement installés dans le profil de session. Pour obtenir la liste complète des colonnes de la table des services de messagerie, consultez la rubrique [message service table](message-service-tables.md).
  
La table des services de messagerie est statique. Une fois qu'un client a reçu l'accès à celui-ci, les ajouts ou suppressions de service de message suivants ne l'affectent pas. S'il n'y a pas de services de messagerie dans le profil actif, **GetMsgServiceTable** renvoie un tableau sans aucune ligne. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnRefreshView  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin:: GetMsgServiceTable** pour charger la table des services dans un profil à afficher dans la vue.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


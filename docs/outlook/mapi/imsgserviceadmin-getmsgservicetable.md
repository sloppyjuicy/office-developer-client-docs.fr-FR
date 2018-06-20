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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 588a32cb2a468c84dfc513af5e4abf6a9a1d0286
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784270"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**S’applique à**: Outlook 
  
Permet d’accéder à la table de service de message, une liste des services dans le profil de message.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Toujours NULL.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau de service de message.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le tableau de service de message a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::GetMsgServiceTable** permet d’accéder à la table de service de message, une table qui gère MAPI qui répertorie les services de message actuellement installées dans le profil de la session. Pour obtenir une liste complète des colonnes de la table de service de message, voir le [Tableau de Service de Message](message-service-tables.md).
  
Le tableau de service de message est statique. Une fois un client est autorisé à accéder à celui-ci, ajouts de service de message qui s’affiche et les suppressions n’affectent pas son. S’il n’y a aucun message les services dans le profil actuel, **GetMsgServiceTable** renvoie un tableau avec des lignes de zéro. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::GetMsgServiceTable** pour charger le tableau des services dans un profil à afficher dans l’affichage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


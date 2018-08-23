---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 834b010dc4810e26264bb418de9630bc83b99810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565290"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table fournisseurs, une liste des fournisseurs de services dans le profil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Toujours NULL.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table des fournisseurs.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le tableau fournisseur a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::GetProviderTable** permet d’accéder à la table du fournisseur MAPI, un tableau qui répertorie le carnet d’adresses, banque de messages et des fournisseurs de transport actuellement installées dans le profil. 
  
Contrairement à la table fournisseur renvoyée par la méthode [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) , la table fournisseur renvoyée par le biais de **IMsgServiceAdmin::GetProviderTable** ne peut pas inclure d’autres lignes qui représentent les informations associées avec un ou plusieurs fournisseurs de services dans le profil. 
  
Fournisseurs qui ont été supprimés, ou sont en cours d’utilisation, ont été marquées pour suppression, mais ne sont pas inclus dans la table fournisseur. Tables du fournisseur sont statiques, ce qui signifie que les compléments suivantes ou les suppressions du profil ne sont pas reflétées dans le tableau. 
  
Si le profil n’a aucun fournisseur, **GetProviderTable** renvoie un tableau avec des lignes de zéro et la valeur de retour de S_OK. 
  
Pour obtenir une liste complète des colonnes de la table fournisseur, voir [Tableau de fournisseur](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour récupérer les lignes d’une table du fournisseur dans l’ordre de transport, utilisez la procédure suivante :
  
1. Appelez la méthode [IMAPITable](imapitable-restrict.md) pour imposer une restriction de propriété qui correspond à la propriété **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) avec MAPI_TRANSPORT_PROVIDER.
    
2. Appelez la méthode [IMAPITable::SortTable](imapitable-sorttable.md) pour trier le tableau par la colonne **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) pour obtenir les lignes du tableau. 
    
Une alternative à ces appels est pour émettre un appel à la fonction [HrQueryAllRows](hrqueryallrows.md) avec toutes les données appropriées structures passés unique. 
  
Si vous récupérez les colonnes **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de chacune des lignes, vous pouvez utiliser ce tableau de structures **MAPIUID** pour définir l’ordre de transport dans un appel à [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ effectue les opérations suivantes : 
  
- Définit le type de chaîne au format Unicode pour les données renvoyées pour les colonnes actives initiales de la table fournisseur par la méthode [IMAPITable::QueryColumns](imapitable-querycolumns.md) . Les colonnes actives initiales pour une table fournisseur sont les colonnes de que la méthode **QueryColumns** renvoie avant que le fournisseur qui contient la table appelle la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- Définit le type de chaîne au format Unicode pour les données renvoyées pour les lignes actives initiales de la table fournisseur par **QueryRows**. Les lignes actives initiales pour une table du fournisseur sont les lignes **que QueryRows** renvoie avant que le fournisseur qui contient la table appelle **SetColumns**. 
    
- Contrôle les types de propriétés de l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) avant que le client qui contient la table fournisseur appelle la méthode [IMAPITable::SortTable](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


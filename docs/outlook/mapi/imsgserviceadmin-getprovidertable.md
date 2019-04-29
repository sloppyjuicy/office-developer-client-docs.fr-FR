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
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428766"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l'accès à la table du fournisseur, une liste des fournisseurs de services dans le profil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Toujours NULL.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table des fournisseurs.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table du fournisseur a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin:: GetProviderTable** fournit l'accès à la table du fournisseur MAPI, un tableau qui répertorie tous les carnets d'adresses, les banques de messages et les fournisseurs de transport actuellement installés dans le profil. 
  
Contrairement à la table du fournisseur renvoyée par la méthode [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md) , la table du fournisseur renvoyée via **IMsgServiceAdmin:: GetProviderTable** ne peut pas inclure de lignes supplémentaires qui représentent les informations associées avec un ou plusieurs fournisseurs de services dans le profil. 
  
Les fournisseurs qui ont été supprimés ou qui sont en cours d'utilisation, mais qui ont été marqués pour suppression, ne sont pas inclus dans la table des fournisseurs. Les tables de fournisseur sont statiques, ce qui signifie que les ajouts ou suppressions ultérieurs du profil ne sont pas répercutés dans le tableau. 
  
Si le profil n'a pas de fournisseurs, **GetProviderTable** renvoie une table avec zéro ligne et la valeur de retour de S_OK. 
  
Pour obtenir la liste complète des colonnes de la table des fournisseurs, voir [Provider table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer les lignes d'une table de fournisseur dans l'ordre de transport, procédez comme suit:
  
1. Appelez la méthode [IMAPITable:: Restrict](imapitable-restrict.md) pour imposer une restriction de propriété qui correspond à la propriété **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) avec MAPI_TRANSPORT_PROVIDER.
    
2. Appelez la méthode [IMAPITable:: SortTable](imapitable-sorttable.md) pour trier le tableau à l'aide de la colonne **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Appelez la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) pour obtenir les lignes de la table. 
    
Une autre solution consiste à effectuer un seul appel à la fonction [HrQueryAllRows](hrqueryallrows.md) avec toutes les structures de données appropriées transmises. 
  
Si vous récupérez les colonnes **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans chacune des lignes, vous pouvez utiliser ce tableau de structures **MAPIUID** pour définir l'ordre de transport dans un appel à [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ effectue les opérations suivantes: 
  
- Définit le type de chaîne à Unicode pour les données renvoyées pour les colonnes initiales actives de la table du fournisseur à l'aide de la méthode [IMAPITable:: QueryColumns](imapitable-querycolumns.md) . Les colonnes initiales actives d'une table de fournisseurs sont les colonnes renvoyées par la méthode **QueryColumns** avant que le fournisseur qui contient la table appelle la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) . 
    
- Définit le type de chaîne à Unicode pour les données renvoyées pour les lignes initiales actives de la table du fournisseur par **QueryRows**. Les lignes initiales actives d'une table de fournisseurs sont les lignes **QueryRows** renvoyées avant que le fournisseur qui contient la table appelle **SetColumns**. 
    
- Contrôle les types de propriétés de l'ordre de tri renvoyé par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) avant que le client qui contient la table de fournisseurs appelle la méthode [IMAPITable:: SortTable](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


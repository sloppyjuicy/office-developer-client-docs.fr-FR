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
  
Permet d’accéder à la table des fournisseurs, qui répertorie les fournisseurs de services dans le profil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Toujours NULL.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau du fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table fournisseur a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::GetProviderTable** permet d’accéder à la table des fournisseurs MAPI, qui répertorie tous les fournisseurs de carnet d’adresses, de magasin de messages et de transport actuellement installés dans le profil. 
  
Contrairement à la table fournisseur renvoyée par le biais de la méthode [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md) la table fournisseur renvoyée via **IMsgServiceAdmin::GetProviderTable** ne peut pas inclure de lignes supplémentaires qui représentent les informations associées à un ou plusieurs fournisseurs de services dans le profil. 
  
Les fournisseurs qui ont été supprimés ou qui sont en cours d’utilisation mais qui ont été marqués pour suppression ne sont pas inclus dans la table des fournisseurs. Les tables de fournisseurs sont statiques, ce qui signifie que les ajouts ou suppressions ultérieurs du profil ne sont pas reflétés dans le tableau. 
  
Si le profil n’a pas de fournisseur, **GetProviderTable** renvoie un tableau avec zéro ligne et la S_OK valeur de retour. 
  
Pour obtenir la liste complète des colonnes dans la table provider, voir [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer les lignes d’une table de fournisseurs dans l’ordre de transport, utilisez la procédure suivante :
  
1. Appelez la [méthode IMAPITable::Restrict](imapitable-restrict.md) pour imposer une restriction de propriété qui correspond à la propriété **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) avec MAPI_TRANSPORT_PROVIDER.
    
2. Appelez la [méthode IMAPITable::SortTable](imapitable-sorttable.md) pour trier le tableau en PR_PROVIDER_ORDINAL **(** [PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Appelez [la méthode IMAPITable::QueryRows](imapitable-queryrows.md) pour obtenir les lignes du tableau. 
    
Une alternative à ces appels consiste à effectuer un appel unique à la fonction [HrQueryAllRows](hrqueryallrows.md) avec toutes les structures de données appropriées transmises. 
  
Si vous récupérez les colonnes **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans chacune des lignes, vous pouvez utiliser ce tableau de structures **MAPIUID** pour définir l’ordre de transport dans un appel à [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
La définition de MAPI_UNICODE’indicateur dans  _le paramètre ulFlags_ permet d': 
  
- Définit le type de chaîne sur Unicode pour les données renvoyées pour les colonnes actives initiales de la table fournisseur par la méthode [IMAPITable::QueryColumns.](imapitable-querycolumns.md) Les colonnes actives initiales d’une table de fournisseur sont les colonnes que la méthode **QueryColumns** renvoie avant que le fournisseur qui contient la table appelle la méthode [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- Définit le type de chaîne sur Unicode pour les données renvoyées pour les lignes actives initiales de la table fournisseur par **QueryRows**. Les premières lignes actives d’une table de fournisseur sont les lignes que **QueryRows** renvoie avant le fournisseur qui contient la table appelle **SetColumns**. 
    
- Contrôle les types de propriétés de l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) avant que le client qui contient la table fournisseur appelle la méthode [IMAPITable::SortTable.](imapitable-sorttable.md) 
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


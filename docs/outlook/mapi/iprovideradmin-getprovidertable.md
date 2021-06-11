---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434472"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table des fournisseurs du service de messagerie, une liste des fournisseurs de services dans le service de messagerie.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées dans les colonnes de la table fournisseur. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les colonnes sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau du fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table fournisseur a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IProviderAdmin::GetProviderTable** récupère un pointeur vers la table des fournisseurs du service de message, une table que MAPI maintient et qui contient des informations sur chaque fournisseur de services dans le service de messagerie. 
  
Contrairement à la table fournisseur renvoyée par la méthode [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) la table fournisseur renvoyée par **IProviderAdmin::GetProviderTable** peut inclure des lignes supplémentaires qui représentent des informations associées à un ou plusieurs fournisseurs de services dans le service de messagerie. Ces informations supplémentaires sont ajoutées au profil avec le mot clé « Sections » du fichier Mapisvc.inf. Lorsqu’un fournisseur possède des sections de profil supplémentaires, il stocke les structures **MAPIUID** pour ces sections dans la propriété **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** est enregistré dans la section profil du service de message. 
  
Les fournisseurs qui ont été supprimés ou qui sont en cours d’utilisation mais qui ont été marqués pour suppression ne sont pas inclus dans la table des fournisseurs. Les tables de fournisseurs sont statiques, ce qui signifie que les ajouts ou suppressions ultérieurs du service de messagerie ne sont pas reflétés dans le tableau. 
  
Si le service de messagerie n’a pas de fournisseur, **IProviderAdmin::GetProviderTable** renvoie un tableau avec zéro ligne et la valeur S_OK renvoyer. 
  
La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
Pour obtenir la liste complète des colonnes dans la table provider, voir [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer les lignes d’une table de fournisseurs dans l’ordre de transport, tez le tableau en PR_PROVIDER_ORDINAL **(** [PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Pour récupérer uniquement les lignes qui représentent des fournisseurs de services (sans inclure de lignes supplémentaires), limitez votre récupération aux lignes qui ont une valeur de PT_ERROR dans leur colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI utilise la méthode **IProviderAdmin::GetProviderTable** pour obtenir la table des fournisseurs à restituer dans une nouvelle boîte de dialogue.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


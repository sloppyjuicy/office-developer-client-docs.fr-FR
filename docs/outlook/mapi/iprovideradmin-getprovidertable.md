---
title: IProviderAdminGetProviderTable
description: IProviderAdmin GetProviderTable fournit l’accès à la table du fournisseur du service de message, une liste des fournisseurs de services dans le service de message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
ms.openlocfilehash: b2a5221d1e2066e28d931c908b9caf6ef873d1de
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828352"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à la table du fournisseur du service de message, une liste des fournisseurs de services dans le service de message.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type des chaînes retournées dans les colonnes de la table du fournisseur. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l’indicateur de MAPI_UNICODE n’est pas défini, les colonnes sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table du fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table du fournisseur a été retournée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin::GetProviderTable** récupère un pointeur vers la table du fournisseur du service de message, une table que MAPI gère qui contient des informations sur chaque fournisseur de services dans le service de message. 
  
Contrairement à la table du fournisseur retournée par la méthode [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , la table de fournisseur retournée par **IProviderAdmin::GetProviderTable** peut inclure des lignes supplémentaires qui représentent des informations associées à un ou plusieurs fournisseurs de services dans le service de message. Ces informations supplémentaires sont ajoutées au profil avec le mot clé « Sections » du fichier Mapisvc.inf. Lorsqu’un fournisseur a des sections de profil supplémentaires, il stocke les structures **MAPIUID** pour ces sections dans la propriété **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** est enregistré dans la section profil de service de message. 
  
Les fournisseurs qui ont été supprimés ou qui sont utilisés mais qui ont été marqués pour suppression ne sont pas inclus dans la table du fournisseur. Les tables du fournisseur sont statiques, ce qui signifie que les ajouts ou suppressions suivants du service de message ne sont pas reflétés dans la table. 
  
Si le service de message n’a aucun fournisseur, **IProviderAdmin::GetProviderTable** retourne une table avec zéro ligne et la valeur de retour S_OK. 
  
La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées à partir des méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . 
  
Cet indicateur contrôle également les types de propriétés dans l’ordre de tri retourné par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
Pour obtenir la liste complète des colonnes de la table du fournisseur, consultez [La table du](provider-tables.md) fournisseur. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer les lignes d’une table de fournisseur dans l’ordre de transport, triez la table par la colonne **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Pour récupérer uniquement les lignes qui représentent les fournisseurs de services (sans inclure de lignes supplémentaires), limitez votre récupération aux lignes qui ont une valeur de PT_ERROR dans leur colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI utilise la méthode **IProviderAdmin::GetProviderTable** pour obtenir la table des fournisseurs à afficher dans une nouvelle boîte de dialogue. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


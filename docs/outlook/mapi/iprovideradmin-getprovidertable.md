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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3ddfcdd95f0423ba92c37c434f18078eadf90d82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594018"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table fournisseur du service de message, une liste des fournisseurs de services dans le service de message.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées dans les colonnes de la table fournisseur. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les colonnes de type chaîne sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table des fournisseurs.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le tableau fournisseur a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin::GetProviderTable** récupère un pointeur vers fournisseur table du service message, qui gère les MAPI qui contient des informations sur chaque fournisseur de services dans le service de message. 
  
Contrairement à la table fournisseur renvoyée par la méthode [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , la table fournisseur renvoyée par **IProviderAdmin::GetProviderTable** peut inclure des lignes supplémentaires qui représentent les informations associées à une ou plusieurs des les fournisseurs de services dans le service de message. Cette information supplémentaire est ajoutée au profil avec le mot clé « Sections » du fichier Mapisvc.inf. Lorsqu’un fournisseur comporte des sections de profil supplémentaires, il stocke les structures **MAPIUID** pour ces sections dans la propriété **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** est enregistré dans la section de profil de service de message. 
  
Fournisseurs qui ont été supprimés, ou sont en cours d’utilisation, ont été marquées pour suppression, mais ne sont pas inclus dans la table fournisseur. Tables du fournisseur sont statiques, ce qui signifie que les ajouts ou les suppressions à partir du service de message ne sont pas reflétées dans la table. 
  
Si le service de message n’a aucun fournisseur, **IProviderAdmin::GetProviderTable** renvoie un tableau avec des lignes de zéro et la valeur de retour de S_OK. 
  
Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . 
  
Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
Pour obtenir une liste complète des colonnes de la table fournisseur, voir [Tableau de fournisseur](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour récupérer les lignes d’une table du fournisseur dans l’ordre de transport, trier le tableau par la colonne **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Pour récupérer uniquement les lignes qui représentent des fournisseurs de services (sans y compris les lignes supplémentaires), limitez votre recherche les lignes qui ont une valeur de PT_ERROR dans la colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI utilise la méthode **IProviderAdmin::GetProviderTable** pour obtenir la table des fournisseurs à afficher dans une boîte de dialogue.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


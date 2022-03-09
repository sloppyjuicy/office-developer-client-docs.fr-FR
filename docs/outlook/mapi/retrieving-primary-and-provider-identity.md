---
title: Récupération de l’identité principale et du fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
ms.openlocfilehash: 46c20201e992856f5f91a56f70f17dbd49656bb8
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371806"
---
# <a name="retrieving-primary-and-provider-identity"></a>Récupération de l’identité principale et du fournisseur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services, généralement des fournisseurs de carnets d’adresses, ont la possibilité de fournir une identité qui peut être utilisée pour représenter la session dans diverses situations. Trois propriétés décrivent l’identité d’un fournisseur :
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Ces propriétés sont définies sur l’identificateur d’entrée, le nom d’affichage et la clé de recherche de l’objet d’identité correspondant, qui est généralement un utilisateur de messagerie. Les fournisseurs qui fournissent une identité définissent également l’STATUS_PRIMARY_IDENTITY dans leur propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
Selon vos besoins, vous pouvez utiliser l’identité d’un fournisseur particulier ou l’identité principale de la session. Vous pouvez également utiliser l’identité d’un fournisseur à des fins d’affichage ou pour récupérer des propriétés, telles que **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, s’il est définie, contient le chemin d’accès aux fichiers utilisés ou créés par le fournisseur. Récupérez **la PR_RESOURCE_PATH** du fournisseur fournissant l’identité principale lorsque vous souhaitez localiser les fichiers qui se rapportent à l’utilisateur de la session. 
  
 **Pour récupérer l’identité d’un fournisseur spécifique**
  
1. [Appelez IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Créez une restriction à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre la colonne **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) au nom du fournisseur spécifié. 
    
3. [Appelez IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne du fournisseur. L’identité du fournisseur est stockée dans la **colonne PR_IDENTITY_ENTRYID, si** elle existe. 
    
 **Pour récupérer l’identité principale d’une session**
  
- [Appelez IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** base l’identité de session sur l’existence de la valeur STATUS_PRIMARY_IDENTITY dans la **colonne PR_RESOURCE_FLAGS’une** des lignes de la table d’état. Si aucune des lignes d’état n’a cette valeur définie, **QueryIdentity** affecte l’identité au premier fournisseur de services qui définit les trois propriétés PR_IDENTITY données. Si aucun fournisseur de services ne fournit d’identité, **QueryIdentity** renvoie MAPI_W_NO_SERVICE. Lorsque cela se produit, vous devez créer une chaîne de caractères pour représenter un utilisateur générique qui peut servir d’identité principale. 
    
 **Pour définir explicitement l’identité principale d’une session**
  
- [Appelez IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Passez le **MAPIUID** pour le fournisseur de services cible. 
    


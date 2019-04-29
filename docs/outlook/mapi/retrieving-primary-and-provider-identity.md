---
title: Récupération de l'identité principale et de l'identité du fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430811"
---
# <a name="retrieving-primary-and-provider-identity"></a>Récupération de l'identité principale et de l'identité du fournisseur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services, généralement les fournisseurs de carnets d'adresses, ont la possibilité de fournir une identité qui peut être utilisée pour représenter la session dans diverses situations. Trois propriétés décrivent l'identité d'un fournisseur:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Ces propriétés sont définies sur l'identificateur d'entrée, le nom d'affichage et la clé de recherche de l'objet Identity correspondant, qui est en général un utilisateur de messagerie. Les fournisseurs qui fournissent une identité définissent également l'indicateur STATUS_PRIMARY_IDENTITY dans leur propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
En fonction de vos besoins, vous pouvez utiliser l'identité d'un fournisseur particulier ou l'identité principale de la session. Vous pouvez également utiliser l'identité d'un fournisseur à des fins d'affichage ou pour récupérer des propriétés, telles que **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, si défini, contient le chemin d'accès aux fichiers utilisés ou créés par le fournisseur. Récupérez la propriété **PR_RESOURCE_PATH** pour le fournisseur qui fournit l'identité principale lorsque vous souhaitez localiser des fichiers qui se rapportent à l'utilisateur de la session. 
  
 **Pour récupérer l'identité d'un fournisseur spécifique**
  
1. Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d'État. 
    
2. Créer une restriction à l'aide d'une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre la colonne **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) avec le nom du fournisseur spécifié. 
    
3. Appelez [IMAPITable:: FindRow](imapitable-findrow.md) pour localiser la ligne du fournisseur. L'identité du fournisseur est stockée dans la colonne **PR_IDENTITY_ENTRYID** , si elle existe. 
    
 **Pour récupérer l'identité principale pour une session**
  
- Appelez [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** base l'identité de session sur l'existence de la valeur STATUS_PRIMARY_IDENTITY dans la colonne **PR_RESOURCE_FLAGS** pour l'une des lignes du tableau d'État. Si aucune des lignes d'État n'a cette valeur définie, **QueryIdentity** affecte l'identité au premier fournisseur de services qui définit les trois propriétés PR_IDENTITY. Si aucun fournisseur de services ne fournit une identité, **QueryIdentity** renvoie MAPI_W_NO_SERVICE. Dans ce cas, vous devez créer une chaîne de caractères qui représente un utilisateur générique qui peut servir d'identité principale. 
    
 **Pour définir explicitement l'identité principale d'une session**
  
- Appelez [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). TransMettez le **MAPIUID** pour le fournisseur de services cible. 
    


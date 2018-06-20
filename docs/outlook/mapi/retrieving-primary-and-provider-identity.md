---
title: Extraction de principal et identité du fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2a87e32fe21aa6fb1d9296c568a74da994c146bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787012"
---
# <a name="retrieving-primary-and-provider-identity"></a>Extraction de principal et identité du fournisseur

  
  
**S’applique à**: Outlook 
  
Fournisseurs de services, généralement les fournisseurs de carnet d’adresses, ont la possibilité de fournir une identité qui peut être utilisée pour représenter la session dans de nombreuses situations. Trois propriétés décrivent l’identité d’un fournisseur :
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Ces propriétés sont définies à l’identificateur d’entrée, un nom d’affichage et une clé de recherche de l’objet d’identité correspondant, qui est généralement un utilisateur de messagerie. Fournisseurs de fournissent une identité également définir l’indicateur STATUS_PRIMARY_IDENTITY dans leur propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
Selon vos besoins, vous pouvez utiliser une identité d’un fournisseur particulier ou le principal pour la session. Vous pouvez utiliser identité d’un fournisseur également pour l’affichage ou pour récupérer les propriétés, telles que **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, si la valeur, contient le chemin d’accès aux fichiers utilisé ou créé par le fournisseur. Récupérer la propriété **PR_RESOURCE_PATH** pour le fournisseur en fournissant l’identité principale lorsque vous souhaitez rechercher des fichiers qui s’appliquent à l’utilisateur de la session. 
  
 **Pour extraire l’identité d’un fournisseur spécifique**
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Créer une restriction à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) pour correspondre à la colonne **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) avec le nom du fournisseur spécifié. 
    
3. Appel [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne du fournisseur. Identité du fournisseur sera stockée dans la colonne **PR_IDENTITY_ENTRYID** , si elle existe. 
    
 **Pour extraire l’identité principale d’une session**
  
- Appelez [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** base identité de la session sur l’existence de la valeur STATUS_PRIMARY_IDENTITY dans la colonne **PR_RESOURCE_FLAGS** pour une des lignes de la table d’état. Si aucune des lignes état ont cette valeur, **QueryIdentity** assigne identité pour le premier fournisseur de services qui définit les trois propriétés PR_IDENTITY. Si aucun fournisseur de services ne fournit une identité, **QueryIdentity** renvoie MAPI_W_NO_SERVICE. Dans ce cas, vous devez créer une chaîne de caractères pour représenter un utilisateur générique qui peut servir à l’identité du principale. 
    
 **Pour définir explicitement l’identité du principale d’une session**
  
- Appelez [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Passez la **MAPIUID** pour le fournisseur de services cible. 
    


---
title: Identité principale MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: de1fe8fd5ef5a6e79934478c62b2403c48f85b5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565878"
---
# <a name="mapi-primary-identity"></a>Identité principale MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La plupart des sessions MAPI ont un fournisseur de services qui fournit l’identité du principale pour la session. En règle générale, il est un fournisseur de carnet d’adresses, qui fournit l’identité par le biais d’une de ses listes de distribution ou les objets utilisateur de messagerie. En fait, MAPI recommande de services de messagerie qui incluent un fournisseur de carnet d’adresses d’utiliser une de ses objets pour l’identité du principale. Lorsqu’un fournisseur de services qui appartient à un service de message fournit l’identité principale, tous les autres fournisseurs de service dans le service message partagent cette identité.
  
Le fichier MAPISVC.inf. Fichier configuration comporte des entrées relatives à l’identité au niveau du service de message et au niveau du fournisseur de service. Sections de service de message doivent inclure une entrée qui indique si le service peut fournir l’identité du principale ; sections de fournisseur de service incluent une entrée similaire uniquement lorsque le fournisseur peut fournir une identité.
  
Le tableau suivant répertorie les entrées qui apparaissent dans les sections de fournisseur de service dans le fichier MAPISVC.inf et le service de message. Fichier.
  
|**Fournisseur d’identité principale**|**Paramètre PR_RESOURCE_FLAGS**|
|:-----|:-----|
|Service de message  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Pas le service de message  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Fournisseur de services  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Bien que plusieurs services de messagerie peuvent déclarer leur capacité à fournir l’identité principale d’une session, service qu’un message est sélectionné. Cette sélection peut se produire :
  
- Lorsque vous créez un profil.
    
- Lorsqu’un client appelle **IMsgServiceAdmin::SetPrimaryIdentity** pour établir explicitement un service de message particulier en tant que le fournisseur de l’identité de la session. Pour plus d’informations. Voir [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Lorsqu’un profil est créé, MAPI désigne le premier service de message à être configuré qui inclut un fournisseur avec l’indicateur STATUS_PRIMARY_IDENTITY dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) pour fournir l’identité du principale . Au sein du service de message spécifique, le premier fournisseur à configurer avec cet indicateur défini de ressources est choisi pour fournir l’identité du service. L’indicateur STATUS_PRIMARY_IDENTITY est désactivée pour tous les autres fournisseurs dans le service désigné et autres services de messagerie dans le profil. Si le fournisseur d’identité principale de fournir à tout moment est supprimé du profil, MAPI attribue le rôle au fournisseur suivant pour configurer qui peut fournir l’identité. Cela est déterminé par l’apparence de la `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` entrée dans la section du fournisseur dans le fichier MAPISVC.INF. 
  
Lorsqu’un client appelle la méthode de **IMsgServiceAdmin::SetPrimaryIdentity** d’un service de message, il spécifie la MAPIUID pour un fournisseur de services au sein du service cible. Pour plus d’informations, voir [MAPIUID](mapiuid.md). Le fournisseur de services représenté par l' **MAPIUID** est affecté à fournir l’identité principale pour le service de message et de la session, et toutes les autres fournisseurs dans le service utilisent cette identité. 
  
Chaque fournisseur dans le service message chargé de fournir l’identité du principale met à jour sa ligne dans la table d’état pour inclure les propriétés suivantes.
  
|**Propriété identité principale**|**Définition sur**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nom complet de l’objet en fournissant l’identité du principale.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Clé de recherche pour l’objet en fournissant l’identité du principale.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificateur d’entrée pour l’objet en fournissant l’identité du principale.  <br/> |
   
 **Pour récupérer l’identificateur d’entrée pour l’objet en fournissant l’identité du principale**
  
- Appelez la méthode **IMAPISession::QueryIdentity** . Pour plus d’informations, voir [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** recherche dans la table d’état de la ligne qui contient la valeur STATUS_PRIMARY_IDENTITY dans la colonne **PR_RESOURCE_FLAGS** et renvoie le correspondant **PR_IDENTITY_ENTRYID** en tant que l’identificateur d’entrée pour le serveur principal identité. 
    


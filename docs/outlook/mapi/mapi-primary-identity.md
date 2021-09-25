---
title: MAPI Primary Identity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dd0ffa1d8c9d2b8b8a65fd8434fc382f6ee77547
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610236"
---
# <a name="mapi-primary-identity"></a>MAPI Primary Identity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des sessions MAPI ont un fournisseur de services particulier qui fournit l’identité principale de la session. En règle générale, il s’agit d’un fournisseur de carnet d’adresses, qui fournit l’identité via l’un de ses objets utilisateur de messagerie ou listes de distribution. En fait, MAPI recommande que les services de messagerie qui incluent un fournisseur de carnet d’adresses utilisent l’un de ses objets pour l’identité principale. Lorsqu’un fournisseur de services appartenant à un service de messagerie fournit l’identité principale, tous les autres fournisseurs de services du service de messagerie partagent cette identité.
  
The MAPISVC. Le fichier de configuration INF possède des entrées relatives à l’identité au niveau du service de messagerie et du fournisseur de services. Les sections du service de message doivent inclure une entrée qui indique si le service peut fournir ou non l’identité principale . Les sections du fournisseur de services incluent une entrée similaire uniquement lorsque le fournisseur peut fournir une identité.
  
Le tableau suivant répertorie les entrées qui apparaissent dans les sections du service de messagerie et du fournisseur de services dans MAPISVC. Fichier INF.
  
|**Fournisseur d’identité principal**|**PR_RESOURCE_FLAGS paramètre**|
|:-----|:-----|
|Service de message  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Pas le service de message  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Fournisseur de services  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Bien que plusieurs services de message peuvent déclarer leur capacité à fournir l’identité principale d’une session, un seul service de message est sélectionné pour le faire. Cette sélection peut se produire :
  
- Lors de la création d’un profil.
    
- Lorsqu’un client appelle **IMsgServiceAdmin::SetPrimaryIdentity** pour établir explicitement un service de message particulier en tant que fournisseur de l’identité de session. Pour plus d’informations. Voir [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Lorsqu’un profil est créé, MAPI désigne le premier service de message à configurer qui inclut un fournisseur avec l’indicateur STATUS_PRIMARY_IDENTITY définie dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) pour fournir l’identité principale. Dans le service de message désigné, le premier fournisseur à être configuré avec cet indicateur de ressource est choisi pour fournir l’identité du service. L STATUS_PRIMARY_IDENTITY est effacé pour tous les autres fournisseurs du service désigné et d’autres services de messagerie dans le profil. Si, à un moment quelconque, le fournisseur fournissant l’identité principale est supprimé du profil, MAPI attribue le rôle au fournisseur suivant à configurer et qui peut fournir l’identité. Cela est déterminé par l’apparence de l’entrée dans la section du fournisseur  `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` dans MAPISVC.INF. 
  
Lorsqu’un client appelle la méthode **IMsgServiceAdmin::SetPrimaryIdentity** d’un service de messagerie, il spécifie le MAPIUID pour un fournisseur de services au sein du service cible. Pour plus d’informations, [voir MAPIUID](mapiuid.md). Le fournisseur de services représenté par **MAPIUID** est affecté pour fournir l’identité principale pour le service de message et pour la session, et tous les autres fournisseurs du service partageront cette identité. 
  
Chaque fournisseur du service de messagerie responsable de la fourniture de l’identité principale met à jour sa ligne dans la table d’état pour inclure les propriétés suivantes.
  
|**Propriété d’identité principale**|**Définition sur**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nom complet de l’objet fournissant l’identité principale.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Clé de recherche de l’objet fournissant l’identité principale.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificateur d’entrée de l’objet fournissant l’identité principale.  <br/> |
   
 **Pour récupérer l’identificateur d’entrée de l’objet fournissant l’identité principale**
  
- Appelez **la méthode IMAPISession::QueryIdentity.** Pour plus d’informations, [voir IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** recherche dans la table d’état la ligne qui contient la valeur STATUS_PRIMARY_IDENTITY dans sa colonne **PR_RESOURCE_FLAGS** et renvoie la **PR_IDENTITY_ENTRYID** correspondante en tant qu’identificateur d’entrée pour l’identité principale. 
    


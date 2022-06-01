---
title: Identité principale MAPI
description: Fournit des informations sur le fichier de configuration d’identité principale MAPI et répertorie les entrées qui apparaissent dans les sections du service de message et du fournisseur de services.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
ms.openlocfilehash: e3ae5afc48084cfaadf62cce1cac081399dbdd90
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818137"
---
# <a name="mapi-primary-identity"></a>Identité principale MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des sessions MAPI ont un fournisseur de services particulier qui fournit l’identité principale de la session. En règle générale, il s’agit d’un fournisseur de carnet d’adresses, qui fournit l’identité via l’un de ses objets utilisateur de messagerie ou listes de distribution. En fait, MAPI recommande que les services de messages qui incluent un fournisseur de carnet d’adresses utilisent l’un de ses objets pour l’identité principale. Lorsqu’un fournisseur de services qui appartient à un service de message fournit l’identité principale, tous les autres fournisseurs de services du service de message partagent cette identité.
  
The MAPISVC. Le fichier de configuration INF contient des entrées relatives à l’identité au niveau du service de message et du fournisseur de services. Les sections du service de message doivent inclure une entrée qui indique si le service peut fournir ou non l’identité principale ; Les sections du fournisseur de services incluent une entrée similaire uniquement lorsque le fournisseur peut fournir une identité.
  
Le tableau suivant répertorie les entrées qui apparaissent dans les sections service de message et fournisseur de services du MAPISVC. Fichier INF.
  
|**Fournisseur d’identité principal**|**paramètre PR_RESOURCE_FLAGS**|
|:-----|:-----|
|Service de message  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Pas le service de message  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Fournisseur  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Bien que plusieurs services de messages puissent déclarer leur capacité à fournir l’identité principale d’une session, un seul service de message est sélectionné pour le faire. Cette sélection peut se produire :
  
- Lors de la création d’un profil.
    
- Lorsqu’un client appelle **IMsgServiceAdmin::SetPrimaryIdentity** pour établir explicitement un service de message particulier en tant que fournisseur de l’identité de session. Pour plus d’informations. Consultez [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Lorsqu’un profil est créé, MAPI désigne le premier service de message à configurer qui inclut un fournisseur avec l’indicateur STATUS_PRIMARY_IDENTITY défini dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) pour fournir l’identité principale. Dans le service de message désigné, le premier fournisseur à être configuré avec ce jeu d’indicateurs de ressources est choisi pour fournir l’identité du service. L’indicateur STATUS_PRIMARY_IDENTITY est effacé pour tous les autres fournisseurs dans le service désigné et les autres services de message dans le profil. Si, à tout moment, le fournisseur fournissant l’identité principale est supprimé du profil, MAPI affecte le rôle au fournisseur suivant à configurer qui peut fournir l’identité. Cela est déterminé par l’apparence de l’entrée  `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` dans la section du fournisseur dans MAPISVC.INF. 
  
Lorsqu’un client appelle la méthode **IMsgServiceAdmin::SetPrimaryIdentity** d’un service de message, il spécifie le MAPIUID d’un fournisseur de services au sein du service cible. Pour plus d’informations, consultez [MAPIUID](mapiuid.md). Le fournisseur de services représenté par **mapIUID** est affecté pour fournir l’identité principale pour le service de message et pour la session, et tous les autres fournisseurs du service partagent cette identité. 
  
Chaque fournisseur du service de message chargé de fournir l’identité principale met à jour sa ligne dans la table d’état pour inclure les propriétés suivantes.
  
|**Propriété d’identité principale**|**Définition sur**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nom d’affichage de l’objet fournissant l’identité principale. |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Clé de recherche de l’objet fournissant l’identité primaire. |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificateur d’entrée pour l’objet fournissant l’identité principale. |
   
 **Pour récupérer l’identificateur d’entrée de l’objet fournissant l’identité primaire**
  
- Appelez la méthode **IMAPISession::QueryIdentity** . Pour plus d’informations, consultez [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** recherche dans la table d’état la ligne qui contient la valeur STATUS_PRIMARY_IDENTITY dans sa colonne **PR_RESOURCE_FLAGS** et retourne le **PR_IDENTITY_ENTRYID** correspondant comme identificateur d’entrée pour l’identité principale. 
    


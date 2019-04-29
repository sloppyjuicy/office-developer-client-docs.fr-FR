---
title: Identité principale MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5bf88de280b012c54d4caaac6bdfe877f476ac37
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404721"
---
# <a name="mapi-primary-identity"></a>Identité principale MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des sessions MAPI disposent d'un fournisseur de services particulier qui fournit l'identité principale pour la session. En règle générale, il s'agit d'un fournisseur de carnets d'adresses, qui fournit l'identité via l'un de ses objets utilisateur de messagerie ou listes de distribution. En fait, MAPI recommande que les services de messagerie qui incluent un fournisseur de carnet d'adresses utilisent l'un de ses objets pour l'identité principale. Lorsqu'un fournisseur de services appartenant à un service de messagerie fournit l'identité principale, tous les autres fournisseurs de services du service de messagerie partagent cette identité.
  
Le MAPISVC. Le fichier de configuration INF comporte des entrées relatives à l'identité au niveau du service de messagerie et du fournisseur de services. Les sections de service de messagerie doivent inclure une entrée qui indique si le service peut fournir ou non l'identité principale; les sections de fournisseur de services incluent une entrée semblable uniquement lorsque le fournisseur peut fournir une identité.
  
Le tableau suivant répertorie les entrées qui apparaissent dans les sections service de messagerie et fournisseur de services dans le MAPISVC. Fichier INF.
  
|**Fournisseur d'identité principal**|**Paramètre PR_RESOURCE_FLAGS**|
|:-----|:-----|
|Service de messagerie  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Pas le service de messagerie  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Fournisseur de services  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Bien que plusieurs services de messagerie puissent déclarer leur capacité à fournir l'identité principale d'une session, un seul service de messagerie est sélectionné. Cette sélection peut se produire:
  
- Lors de la création d'un profil.
    
- Lorsqu'un client appelle **IMsgServiceAdmin:: SetPrimaryIdentity** pour établir explicitement un service de messagerie particulier en tant que fournisseur de l'identité de session. Pour plus d'informations. Voir [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Lors de la création d'un profil, MAPI désigne le premier service de message à configurer qui inclut un fournisseur avec l'indicateur STATUS_PRIMARY_IDENTITY défini dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) pour fournir l'identité principale. . Dans le service de messagerie désigné, le premier fournisseur à configurer avec cet indicateur de ressource défini est choisi pour fournir l'identité du service. L'indicateur STATUS_PRIMARY_IDENTITY est désactivé pour tous les autres fournisseurs du service désigné et d'autres services de messagerie dans le profil. Si, à tout moment, le fournisseur qui fournit l'identité principale est supprimé du profil, MAPI affecte le rôle au fournisseur suivant à configurer qui peut fournir une identité. Cela est déterminé par l'apparence de l' `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` entrée dans la section du fournisseur dans MAPISVC. inf. 
  
Lorsqu'un client appelle la méthode **IMsgServiceAdmin:: SetPrimaryIdentity** du service de messagerie, il spécifie le MAPIUID pour un fournisseur de services dans le service cible. Pour plus d'informations, consultez la rubrique [MAPIUID](mapiuid.md). Le fournisseur de services représenté par **MAPIUID** est affecté pour fournir l'identité principale pour le service de messagerie et pour la session, et tous les autres fournisseurs dans le service partageront cette identité. 
  
Chaque fournisseur du service de messagerie responsable de la fourniture de l'identité principale met à jour sa ligne dans la table d'État pour inclure les propriétés suivantes.
  
|**Propriété Identity principale**|**Définition sur**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nom complet de l'objet qui fournit l'identité principale.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Clé de recherche pour l'objet qui fournit l'identité principale.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificateur de l'objet qui fournit l'identité principale.  <br/> |
   
 **Pour récupérer l'identificateur d'entrée pour l'objet fournissant l'identité principale**
  
- Appelez la méthode **IMAPISession:: QueryIdentity** . Pour plus d'informations, voir [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** recherche dans la table d'État la ligne qui contient la valeur STATUS_PRIMARY_IDENTITY dans sa colonne **PR_RESOURCE_FLAGS** et renvoie le **PR_IDENTITY_ENTRYID** correspondant comme identificateur d'entrée pour le principal identification. 
    


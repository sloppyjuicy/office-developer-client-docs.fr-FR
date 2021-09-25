---
title: Ouverture des entrées du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f18ba37549f0ea6ee1a4dfa4028fb71289bae274
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600728"
---
# <a name="opening-address-book-entries"></a>Ouverture des entrées du carnet d’adresses

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un client ou un fournisseur a demandé l’ouverture d’un de vos objets, MAPI appelle la méthode [IABLogon::OpenEntry](iablogon-openentry.md) de votre fournisseur. MAPI détermine que l’identificateur d’entrée représentant l’objet cible appartient à votre fournisseur en examinant la partie [MAPIUID](mapiuid.md) de l’identificateur d’entrée et en la faisant correspondre au **MAPIUID** que votre fournisseur a inscrit dans l’appel à **IMAPISupport::SetProviderUID**. MAPI appelle ensuite votre **méthode OpenEntry.** Votre fournisseur doit répondre en récupérant l’objet correspondant ( conteneur, liste de distribution ou utilisateur de messagerie). 
  
Un identificateur d’entrée NULL indique une demande d’ouverture du conteneur racine du fournisseur de carnet d’adresses. Les clients ouvrent le conteneur racine pour accéder à sa table hiérarchique et à ses destinataires. Les fournisseurs de carnet d’adresses qui fournissent uniquement des modèles pour la création de destinataires unique ne prennent pas en charge l’appel **OpenEntry** pour le conteneur racine. 
  
### <a name="to-implement-iablogonopenentry"></a>Pour implémenter IABLogon::OpenEntry
  
1. Vérifiez que l’identificateur d’entrée est un identificateur valide que votre fournisseur prend en charge. S’il ne s’agit pas d’un identificateur d’entrée valide, MAPI_E_INVALID_ENTRYID. 
    
2. Vérifiez l’indicateur transmis avec le _paramètre ulFlags._ Si MAPI est passé en MAPI_MODIFY et que votre fournisseur n’autorise pas la modification de ses objets, échouez et renvoyez la valeur MAPI_E_ACCESS_DENIED’erreur. 
    
3. Vérifiez que l’interface demandée dans  _le paramètre lpInterface_ est valide pour le type d’objet que votre fournisseur a été invité à ouvrir. Si un paramètre non valide a été passé, échouez et renvoyez la valeur MAPI_E_INTERFACE_NOT_SUPPORTED’erreur. 
    
4. Si le  _paramètre cbEntryID_ est zéro, il s’agit d’une demande d’ouverture du conteneur racine de votre fournisseur. Créez le conteneur racine et renvoyez un pointeur vers son **implémentation d’interface IABContainer.** 
    
5. Si votre fournisseur implémente plusieurs objets d’inscription, chacun avec son propre **MAPIUID** enregistré, mapmez le **MAPIUID** contenu dans l’identificateur d’entrée avec l’objet d’inscription approprié. 
    
6. Déterminez le type d’objet représenté par l’identificateur d’entrée : un utilisateur de messagerie, une liste de distribution ou un conteneur appartenant à votre fournisseur ou un utilisateur de messagerie unique ou une liste de distribution afin que la valeur appropriée puisse être définie pour le paramètre _lpulObjectType._ 
    
7. Créez l’objet du type approprié et définissez les propriétés de base suivantes :
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calculez **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à partir des informations dans l’identificateur d’entrée.
    
9. Renvoyer un pointeur vers l’implémentation de l’interface pour l’objet. 
    


---
title: Entrées de carnet d’adresses de l’ouverture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c36c70eacffcb4a41af0e73eea85143ab737867f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784941"
---
# <a name="opening-address-book-entries"></a>Entrées de carnet d’adresses de l’ouverture

**S’applique à**: Outlook 
  
Lorsqu’un client ou le fournisseur a demandé qu’un de vos objets s’ouvre, MAPI appelle la méthode [IABLogon::OpenEntry](iablogon-openentry.md) de votre fournisseur. MAPI détermine que l’identificateur d’entrée qui représente l’objet cible appartient à votre fournisseur en examinant la partie [MAPIUID](mapiuid.md) de l’identificateur d’entrée et en correspondance avec la **MAPIUID** que votre fournisseur inscrit dans l’appel à ** IMAPISupport::SetProviderUID**. MAPI appelle ensuite la méthode **OpenEntry** . Votre fournisseur doit répondre en récupérant l’objet correspondant, un conteneur, une liste de distribution ou un utilisateur de messagerie. 
  
Un identificateur d’entrée NULL indique une demande pour ouvrir le conteneur de racine du fournisseur de carnet d’adresses. Clients d’ouvrir le conteneur racine pour accéder à la table de hiérarchie et ses destinataires. Fournisseurs de carnet d’adresses qui fournit uniquement des modèles pour la création de destinataires uniques ne prennent pas en charge l’appel de **OpenEntry** pour le conteneur racine. 
  
### <a name="to-implement-iablogonopenentry"></a>Pour mettre en œuvre IABLogon::OpenEntry
  
1. Vérifiez que l’identificateur d’entrée est un identificateur valid de votre fournisseur prend en charge. Si elle n’est pas un identificateur d’entrée valide, renvoyer MAPI_E_INVALID_ENTRYID. 
    
2. Vérifiez l’indicateur qui est passé avec le paramètre _ulFlags_ . Si MAPI n’a passé et votre fournisseur n’autorise pas ses objets à modifier, échouer et retourner la valeur d’erreur MAPI_E_ACCESS_DENIED. 
    
3. Vérifiez que l’interface demandée dans le paramètre _lpInterface_ est valide pour le type d’objet de que votre fournisseur a été invité à ouvrir. Si un paramètre non valide a été passé, échouer et retourner la valeur d’erreur MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
4. Si le paramètre _cbEntryID_ est égale à zéro, il s’agit d’une demande d’ouverture du conteneur racine de votre fournisseur. Créer le conteneur racine et renvoyer un pointeur vers son implémentation d’interface **IABContainer** . 
    
5. Si votre fournisseur implémente plusieurs objets d’ouverture de session, chacun avec son propre inscrit **MAPIUID**, carte la **MAPIUID** contenus dans l’identificateur d’entrée avec l’objet d’ouverture de session approprié. 
    
6. Déterminer le type d’objet l’identificateur d’entrée représente : un utilisateur, liste de distribution ou conteneur appartenant à votre fournisseur ou une liste unique d’utilisateur ou de distribution de messagerie afin que la valeur appropriée peut être définie pour le _lpulObjectType_ de messagerie paramètre. 
    
7. Créer l’objet du type approprié et définissez les propriétés de base suivantes :
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calculer **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à partir des informations dans l’identificateur d’entrée.
    
9. Retourne un pointeur vers l’implémentation d’interface pour l’objet. 
    


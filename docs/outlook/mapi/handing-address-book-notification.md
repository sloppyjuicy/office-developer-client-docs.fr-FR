---
title: Notification de carnet d’adresse de remise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b5428ccde0e16bd32408b2ea908f5c5522992fc9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582916"
---
# <a name="handing-address-book-notification"></a>Notification de carnet d’adresse de remise
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Notifications de carnet d’adresse permettent à un client d’événements qui se produisent sur une entrée de carnet d’adresse ou à une entrée particulière. Vous pouvez vous inscrire pour les notifications par le biais du carnet d’adresses MAPI en appelant [IAddrBook::Advise](iaddrbook-advise.md) ou hiérarchie d’un conteneur carnet d’adresses ou une table des matières en appelant [IMAPITable::Advise](imapitable-advise.md). 
  
Spécifier l’identificateur d’entrée d’un conteneur de carnet d’adresses, une liste de distribution ou un utilisateur de messagerie si vous vous inscrivez pour les notifications sur une entrée particulière et la valeur NULL si l’inscription des notifications dans le carnet d’adresses. L’identificateur d’entrée doit représenter un utilisateur de messagerie ou d’une liste de distribution dans un conteneur de carnet d’adresses. **IAddrBook::Advise** examine cet identificateur d’entrée pour déterminer quelle adresse fournisseur de carnet d’est responsable de l’objet correspondant et transfère l’appel à la méthode de [IABLogon::Advise](iablogon-advise.md) du fournisseur livre adresse appropriée. 
  
Les clients peuvent s’inscrire pour les types suivants d’événements sur les entrées de carnet d’adresses :
  
- Erreur critique
    
- Un des événements de l’objet (création, modifié, supprimé, déplacé ou copié)
    
- Table modifiée
    
En règle générale, l’enregistrement se produit uniquement sur le contenu de conteneur du carnet d’adresses et les tables de hiérarchie. Il est rare que les clients s’inscrire avec l’objets de liste de distribution et d’utilisateurs de messagerie de niveau inférieur. Il s’agit, car :
  
- Plusieurs fournisseurs de carnet d’adresses n’acceptent pas les notifications dans leurs listes de distribution et les utilisateurs de messagerie.
    
- Notifications de table sont suffisantes pour le suivi des modifications et les signaler aux utilisateurs.
    


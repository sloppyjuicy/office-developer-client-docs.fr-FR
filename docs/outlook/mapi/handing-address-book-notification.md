---
title: Gestion des notifications du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
ms.openlocfilehash: 127dc0b6d1c72b3540b49df64d2d50bcd75a49eb
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372317"
---
# <a name="handing-address-book-notification"></a>Gestion des notifications du carnet d’adresses
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications de carnet d’adresses permettent à un client d’en savoir plus sur les événements qui se produisent à une entrée de carnet d’adresses ou à une entrée particulière. Vous pouvez vous inscrire à ces notifications via le carnet d’adresses MAPI en appelant [IAddrBook::Advise](iaddrbook-advise.md) ou via la hiérarchie ou la table des matières d’un conteneur de carnet d’adresses en appelant [IMAPITable::Advise](imapitable-advise.md). 
  
Spécifiez l’identificateur d’entrée d’un conteneur de carnet d’adresses, d’une liste de distribution ou d’un utilisateur de messagerie si vous vous inscrivez pour des notifications sur une entrée particulière et NULL si vous vous inscrivez pour les notifications sur l’intégralité du carnet d’adresses. L’identificateur d’entrée doit représenter un utilisateur de messagerie ou une liste de distribution dans un conteneur de carnet d’adresses. **IAddrBook::Advise** examine cet identificateur d’entrée pour déterminer quel fournisseur de carnet d’adresses est responsable de l’objet correspondant et le fait suivre à la méthode [IABLogon::Advise](iablogon-advise.md) du fournisseur de carnet d’adresses approprié. 
  
Les clients peuvent s’inscrire aux types d’événements suivants sur les entrées de carnet d’adresses :
  
- Erreur critique
    
- L’un des événements d’objet (créé, modifié, supprimé, déplacé ou copié)
    
- Tableau modifié
    
En règle générale, l’inscription se produit uniquement sur le contenu du conteneur de carnet d’adresses et les tables hiérarchiques. Il est rare que les clients s’inscrivent avec l’utilisateur de messagerie de niveau inférieur et les objets de liste de distribution. Cela est dû aux raisons :
  
- De nombreux fournisseurs de carnets d’adresses ne peuvent pas prendre en charge les notifications sur leurs utilisateurs de messagerie et leurs listes de distribution.
    
- Les notifications de tableau sont suffisantes pour suivre les modifications et les signaler aux utilisateurs.
    


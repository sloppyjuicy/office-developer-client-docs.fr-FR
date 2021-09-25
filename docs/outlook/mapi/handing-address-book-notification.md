---
title: Gestion des notifications du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a5d3114d3aa01ec20783393b7831f7c661f65adf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551533"
---
# <a name="handing-address-book-notification"></a>Gestion des notifications du carnet d’adresses
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications de carnet d’adresses permettent à un client d’apprendre les événements qui se produisent à une entrée de carnet d’adresses ou à une entrée particulière. Vous pouvez vous inscrire à ces notifications via le carnet d’adresses MAPI en appelant [IAddrBook::Advise](iaddrbook-advise.md) ou via la hiérarchie ou la table des matières d’un conteneur de carnet d’adresses en appelant [IMAPITable::Advise](imapitable-advise.md). 
  
Spécifiez l’identificateur d’entrée d’un conteneur de carnet d’adresses, d’une liste de distribution ou d’un utilisateur de messagerie si vous vous inscrivez pour des notifications sur une entrée particulière et NULL si vous vous inscrivez pour les notifications sur l’intégralité du carnet d’adresses. L’identificateur d’entrée doit représenter un utilisateur de messagerie ou une liste de distribution dans un conteneur de carnet d’adresses. **IAddrBook::Advise** examine cet identificateur d’entrée pour déterminer quel fournisseur de carnet d’adresses est responsable de l’objet correspondant et le fait suivre à la méthode [IABLogon::Advise](iablogon-advise.md) du fournisseur de carnet d’adresses approprié. 
  
Les clients peuvent s’inscrire aux types d’événements suivants sur les entrées de carnet d’adresses :
  
- Erreur critique
    
- L’un des événements d’objet (créé, modifié, supprimé, déplacé ou copié)
    
- Tableau modifié
    
En règle générale, l’inscription se produit uniquement sur le contenu du conteneur de carnet d’adresses et les tables hiérarchiques. Il est rare que les clients s’inscrivent avec l’utilisateur de messagerie de niveau inférieur et les objets de liste de distribution. Cela est dû aux raisons :
  
- De nombreux fournisseurs de carnets d’adresses ne peuvent pas prendre en charge les notifications sur leurs utilisateurs de messagerie et leurs listes de distribution.
    
- Les notifications de tableau sont suffisantes pour suivre les modifications et les signaler aux utilisateurs.
    


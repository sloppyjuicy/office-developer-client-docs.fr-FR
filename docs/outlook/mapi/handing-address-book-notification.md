---
title: Gestion des notifications du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299502"
---
# <a name="handing-address-book-notification"></a>Gestion des notifications du carnet d’adresses
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications de carnet d'adresses permettent à un client d'apprendre des événements qui se produisent à n'importe quelle entrée de carnet d'adresses ou à une entrée particulière. Vous pouvez vous inscrire pour ces notifications via le carnet d'adresses MAPI en appelant [IAddrBook:: Advise](iaddrbook-advise.md) ou par le biais de la table de hiérarchie ou de contenu du conteneur du carnet d'adresses en appelant la méthode [IMAPITable:: Advise](imapitable-advise.md). 
  
Spécifiez l'identificateur d'entrée d'un conteneur de carnet d'adresses, d'une liste de distribution ou d'un utilisateur de messagerie si vous vous inscrivez pour des notifications sur une entrée particulière et si vous vous inscrivez pour des notifications sur l'ensemble du carnet d'adresses. L'identificateur d'entrée doit représenter un utilisateur de messagerie ou une liste de distribution dans un conteneur de carnet d'adresses. **IAddrBook:: Advise** examine cet identificateur d'entrée pour déterminer quel fournisseur de carnet d'adresses est responsable de l'objet correspondant et transfère l'appel à la méthode [IABLogon:: Advise](iablogon-advise.md) du fournisseur de carnet d'adresses approprié. 
  
Les clients peuvent s'inscrire aux types d'événements suivants sur les entrées du carnet d'adresses:
  
- Erreur critique
    
- Tous les événements d'objet (créés, modifiés, supprimés, déplacés ou copiés)
    
- Table modifiée
    
En règle générale, l'inscription se produit uniquement sur le contenu du conteneur du carnet d'adresses et les tables de hiérarchie. Il est rare que les clients s'inscrivent auprès de l'utilisateur de messagerie de niveau inférieur et les objets de liste de distribution. Cela est dû au fait que:
  
- De nombreux fournisseurs de carnets d'adresses ne prennent pas en charge les notifications sur leurs utilisateurs de messagerie et leurs listes de distribution.
    
- Les notifications de table sont suffisantes pour suivre les modifications et les signaler aux utilisateurs.
    


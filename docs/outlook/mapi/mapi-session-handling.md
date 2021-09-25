---
title: Gestion de Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 24a3c7bf89d23cddb6dda5344b01aead2ca38a3a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575504"
---
# <a name="mapi-session-handling"></a>Gestion de Session MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de pouvoir communiquer avec les fournisseurs de services et un système de messagerie sous-jacent, vous devez établir une session. Une session MAPI est un lien entre un client et d’autres composants MAPI. Suite au démarrage réussi d’une session, MAPI renvoie aux clients un pointeur vers un objet de session , un objet qui implémente l’interface **IMAPISession.** Pour plus d’informations, [voir IMAPISession : IUnknown](imapisessioniunknown.md). Vous pouvez utiliser les méthodes de l’interface **IMAPISession** pour accéder aux objets des fournisseurs de carnet d’adresses et de magasins de messages, accéder à plusieurs tables, afficher des formulaires, définir des propriétés de fournisseur de transport et effectuer l’administration de service de profil et de message. 
  
## <a name="in-this-section"></a>Dans cette section

[Démarrage d’une session MAPI](starting-a-mapi-session.md)
  
> Décrit comment démarrer une session MAPI et inclut des liens vers des rubriques avec des informations plus détaillées.
    
[Fin d’une session MAPI](ending-a-mapi-session.md)
  
> Décrit comment mettre fin à une session MAPI.
    
[Accès aux objets à l’aide de la session](accessing-objects-by-using-the-session.md)
  
> Décrit comment utiliser un pointeur de session pour accéder aux objets de session.
    
[Récupération de l’identité principale et du fournisseur](retrieving-primary-and-provider-identity.md)
  
> Décrit les propriétés utilisées pour récupérer l’identité principale et l’identité du fournisseur.
    
[Tableau d’état et objets d’état](status-table-and-status-objects.md)
  
> Décrit comment accéder aux informations à partir du tableau d’état.
    


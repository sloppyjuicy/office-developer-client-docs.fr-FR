---
title: Gestion de Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8c82ff28dca4fc50c7801a533f7ad757b839cddf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568230"
---
# <a name="mapi-session-handling"></a>Gestion de Session MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour pouvoir communiquer avec les fournisseurs de services et un système de messagerie sous-jacent, vous devez établir une session. Une session MAPI est un lien à partir d’un client à d’autres composants MAPI. Comme le résultat de démarrage d’une session MAPI renvoie aux clients un pointeur vers un objet de session, un objet qui implémente l’interface **IMAPISession** . Pour plus d’informations, voir [IMAPISession : IUnknown](imapisessioniunknown.md). Vous pouvez utiliser les méthodes de l’interface **IMAPISession** pour accéder aux objets de fournisseurs de magasins de messages et du carnet d’adresses, accéder à plusieurs tables, afficher des formulaires, définir des propriétés du fournisseur de transport et effectuer l’administration du service de profil et le message. 
  
## <a name="in-this-section"></a>Dans cette section

[Démarrage d’une session MAPI](starting-a-mapi-session.md)
  
> Décrit comment démarrer une session MAPI et inclut des liens vers des rubriques contenant des informations plus détaillées.
    
[Fermeture d’une session MAPI](ending-a-mapi-session.md)
  
> Décrit comment mettre fin à une session MAPI.
    
[Accès aux objets en utilisant une session](accessing-objects-by-using-the-session.md)
  
> Décrit comment utiliser un pointeur de session pour accéder aux objets de la session.
    
[Récupération de l’identité fournisseur et principale](retrieving-primary-and-provider-identity.md)
  
> Décrit les propriétés utilisées pour extraire le principal et l’identité du fournisseur.
    
[Table de statut et objets de statut](status-table-and-status-objects.md)
  
> Décrit comment accéder aux informations à partir de la table d’état.
    


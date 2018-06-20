---
title: Gestion de Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784702"
---
# <a name="mapi-session-handling"></a>Gestion de Session MAPI

  
  
**S’applique à**: Outlook 
  
Pour pouvoir communiquer avec les fournisseurs de services et un système de messagerie sous-jacent, vous devez établir une session. Une session MAPI est un lien à partir d’un client à d’autres composants MAPI. Comme le résultat de démarrage d’une session MAPI renvoie aux clients un pointeur vers un objet de session, un objet qui implémente l’interface **IMAPISession** . Pour plus d’informations, voir [IMAPISession : IUnknown](imapisessioniunknown.md). Vous pouvez utiliser les méthodes de l’interface **IMAPISession** pour accéder aux objets de fournisseurs de magasins de messages et du carnet d’adresses, accéder à plusieurs tables, afficher des formulaires, définir des propriétés du fournisseur de transport et effectuer l’administration du service de profil et le message. 
  
## <a name="in-this-section"></a>Dans cette section

[Démarrage d’une Session MAPI](starting-a-mapi-session.md)
  
> Décrit comment démarrer une session MAPI et inclut des liens vers des rubriques contenant des informations plus détaillées.
    
[Mettre fin à une Session MAPI](ending-a-mapi-session.md)
  
> Décrit comment mettre fin à une session MAPI.
    
[Accès aux objets à l’aide de la Session](accessing-objects-by-using-the-session.md)
  
> Décrit comment utiliser un pointeur de session pour accéder aux objets de la session.
    
[Extraction de principal et identité du fournisseur](retrieving-primary-and-provider-identity.md)
  
> Décrit les propriétés utilisées pour extraire le principal et l’identité du fournisseur.
    
[Table d’état et les objets d’état](status-table-and-status-objects.md)
  
> Décrit comment accéder aux informations à partir de la table d’état.
    


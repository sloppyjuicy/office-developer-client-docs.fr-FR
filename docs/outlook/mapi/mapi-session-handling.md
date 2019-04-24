---
title: Gestion de Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328223"
---
# <a name="mapi-session-handling"></a>Gestion de Session MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de pouvoir communiquer avec des fournisseurs de services et un système de messagerie sous-jacent, vous devez établir une session. Une session MAPI est un lien entre un client et d'autres composants MAPI. Suite à la réussite du démarrage d'une session, MAPI renvoie aux clients un pointeur vers un objet session, un objet qui implémente l'interface **IMAPISession** . Pour plus d'informations, consultez la rubrique [IMAPISession: IUnknown](imapisessioniunknown.md). Vous pouvez utiliser les méthodes de l'interface **IMAPISession** pour accéder aux objets des fournisseurs de carnet d'adresses et de banque de messages, accéder à plusieurs tables, afficher des formulaires, définir des propriétés de fournisseur de transport et effectuer des tâches de profil et de service de messagerie. 
  
## <a name="in-this-section"></a>Contenu de cette section

[Démarrage d'une session MAPI](starting-a-mapi-session.md)
  
> Décrit comment démarrer une session MAPI et inclut des liens vers des rubriques contenant des informations plus détaillées.
    
[Fermeture d'une session MAPI](ending-a-mapi-session.md)
  
> Décrit comment mettre fin à une session MAPI.
    
[Accès aux objets à l'aide de la session](accessing-objects-by-using-the-session.md)
  
> Indique comment utiliser un pointeur de session pour accéder aux objets session.
    
[Récupération de l'identité principale et de l'identité du fournisseur](retrieving-primary-and-provider-identity.md)
  
> Décrit les propriétés utilisées pour extraire l'identité principale et l'identité du fournisseur.
    
[Table d'État et objets d'État](status-table-and-status-objects.md)
  
> Indique comment accéder aux informations à partir de la table d'État.
    


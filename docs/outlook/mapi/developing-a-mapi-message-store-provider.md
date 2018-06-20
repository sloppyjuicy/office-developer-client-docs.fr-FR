---
title: Développement d’un fournisseur de magasin de message MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 040c851d64f60c319250fd0e08620285b6f2f0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783168"
---
# <a name="developing-a-mapi-message-store-provider"></a>Développement d’un fournisseur de magasin de message MAPI
  
**S’applique à**: Outlook 
  
Comme les autres fournisseurs de services MAPI, les banques de messages sont des bibliothèques de liens dynamiques (DLL) qui présentent les services d’un mécanisme de stockage sous-jacent pour les applications clientes MAPI et le spouleur MAPI. Le fournisseur de banque de message présente le mécanisme de stockage sous-jacent comme un ensemble hiérarchique de dossiers et messages utilisable par les clients MAPI et le spouleur MAPI.
  
L’illustration suivante montre l’architecture de banque de message MAPI base.
  
**Architecture de banque de messages**
  
![Architecture de banque de messages] (media/storearc.gif "Architecture de banque de messages")
  
Vous pouvez implémenter un fournisseur de banque de messages à l’aide de n’importe quel type de mécanisme de stockage sous-jacent que. Toutefois, vous devez être conscient des problèmes de performances. En outre, le mécanisme de stockage sous-jacent doit être présenté comme un ensemble hiérarchique d’objets MAPI. Ces exigences signifient que les banques de messages sont généralement implémentés à l’aide d’un produit de base de données existant qui prend en charge le stockage hiérarchique d’objets dans la base de données et qui a une interface de programmation ou une structure de fichier bien définie. Par exemple, les bases de données Microsoft Office Access, SQL et Oracle peuvent servir le mécanisme de stockage sous-jacent. Certains produits de base de données ont des jeux de fonctionnalités qui facilitent la mettre en œuvre des fonctionnalités MAPI, votre choix de la base de données peut-être être affectée par les fonctionnalités de votre fournisseur de magasin de message doit prendre en charge.
  
À l’aide d’une base de données en tant que l’enregistre de mécanisme de stockage sous-jacent que vous travaillez, car il est généralement plus facile de présenter les objets de base de données aux clients MAPI en tant qu’objets MAPI que d’implémenter votre propre mécanisme de stockage hiérarchique. Cela vous permet de traiter des opérations MAPI à un niveau supérieur si vous implémentez votre propre mécanisme de stockage hiérarchique. Par exemple, recherche d’un message avec une ligne de sujet particulier est assez simple de construction et soumettre une requête de base de données appropriée, plutôt que l’implémentation de routines complexes pour rechercher votre mécanisme de stockage hiérarchique.
  
Fournisseurs de magasins message communiquent avec les clients MAPI et le spouleur MAPI pour effectuer des opérations sur les dossiers et les objets. Le fournisseur de banque de messages traduit ces opérations en opérations de bas niveau sur le mécanisme de stockage sous-jacent. Le spouleur MAPI généralement communique avec le fournisseur de banque de message lors de l’envoi et réception de messages. En règle générale, les clients MAPI communiquent avec des fournisseurs de banque de messages pour manipuler la hiérarchie de dossiers et pour lire, modifier, supprimer et envoyer des messages.
  
Le spouleur MAPI et clients MAPI communiquent avec le fournisseur de banque de messages pour créer de nouveaux messages. Applications clientes cela lorsque l’utilisateur compose un message. Le spouleur MAPI cela lorsqu’il reçoit un message entrant. Dans les deux cas, le nouveau message est généralement créé dans le dossier boîte de réception de la banque de messages, le cas échéant.
  
Fournisseurs de banque de message utilisent beaucoup de tables, les dossiers, les messages et les propriétés MAPI. Les détails d’implémentation de ces objets sont documentées dans les [Tableaux MAPI](mapi-tables.md), [Dossiers MAPI](mapi-folders.md), [Messages MAPI](mapi-messages.md)et [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md). Vous devez vous familiariser avec cette documentation avant d’essayer d’implémenter un fournisseur de magasin de message.
  
Il existe deux types d’importantes de fournisseurs de magasins de message : ceux qui peut agir comme valeur par défaut d’un utilisateur de message store et ceux qui ne peuvent pas. Une banque de messages par défaut est 1 dans laquelle les applications et le spouleur MAPI peuvent effectuer toute tâche de messagerie, tels que la réception de messages ou en créant des dossiers. Un fournisseur de magasins de message par défaut doit prendre en charge plusieurs fonctionnalités plus que le nombre minimal requis pour tous les fournisseurs de banque de messages.
  
## <a name="see-also"></a>Voir aussi

- [Concepts MAPI](mapi-concepts.md)


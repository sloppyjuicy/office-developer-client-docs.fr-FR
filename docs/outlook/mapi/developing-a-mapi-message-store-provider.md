---
title: Développement d’un fournisseur de banques de messages MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 76332b57b2957b5682efb415121ea6db42409c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412610"
---
# <a name="developing-a-mapi-message-store-provider"></a>Développement d’un fournisseur de banques de messages MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Comme d’autres fournisseurs de services MAPI, les magasins de messages sont des bibliothèques de liens dynamiques (DLL) qui présentent les services d’un mécanisme de stockage sous-jacent aux applications clientes MAPI et aupooler MAPI. Le fournisseur de magasin de messages présente le mécanisme de stockage sous-jacent sous la forme d’un ensemble hiérarchique de dossiers et de messages que les clients MAPI et lepoolur MAPI peuvent utiliser.
  
L’illustration suivante illustre l’architecture de base de la boutique de messages MAPI.
  
**Architecture de banque de messages**
  
![Architecture de la boutique de messages -]Architecture de la boutique de(media/storearc.gif "messages")
  
Vous pouvez implémenter un fournisseur de magasins de messages à l’aide de n’importe quel type de mécanisme de stockage sous-jacent que vous aimez. Toutefois, vous devez être conscient des problèmes de performances. En outre, le mécanisme de stockage sous-jacent doit être présenté comme une collection hiérarchique d’objets MAPI. Ces exigences signifient que les banques de messages sont généralement implémentées à l’aide d’un produit de base de données existant qui prend en charge le stockage hiérarchique des objets dans la base de données et qui possède une interface de programmation ou une structure de fichiers bien définie. Par exemple, Microsoft Office bases de données Access, SQL et Oracle peuvent être utilisées comme mécanisme de stockage sous-jacent. Certains produits de base de données ont des ensembles de fonctionnalités qui facilitent l’implémenter des fonctionnalités MAPI, de sorte que votre choix de produit de base de données peut être affecté par les fonctionnalités que votre fournisseur de banque de messages doit prendre en charge.
  
L’utilisation d’une base de données existante comme mécanisme de stockage sous-jacent vous permet de gagner du travail, car il est généralement plus facile de présenter des objets de base de données aux clients MAPI en tant qu’objets MAPI que d’implémenter votre propre mécanisme de stockage hiérarchique. Cela vous permet de traiter les opérations MAPI à un niveau plus élevé que si vous implémentez votre propre mécanisme de stockage hiérarchique. Par exemple, la recherche d’un message avec une ligne d’objet particulière devient une question relativement simple de construction et d’envoi d’une requête de base de données appropriée, plutôt que d’implémenter des routines complexes pour rechercher votre mécanisme de stockage hiérarchique.
  
Les fournisseurs de magasins de messages communiquent avec les clients MAPI et lepooler MAPI pour effectuer des opérations sur des dossiers et des objets. Le fournisseur de magasin de messages traduit ces opérations en opérations de niveau inférieur sur le mécanisme de stockage sous-jacent. Lepooler MAPI communique généralement avec le fournisseur de la boutique de messages lors de l’envoi et de la réception de messages. Les clients MAPI communiquent généralement avec les fournisseurs de magasins de messages pour manipuler la hiérarchie de dossiers et pour lire, modifier, supprimer et envoyer des messages.
  
Lepooler MAPI et les clients MAPI communiquent avec le fournisseur de magasins de messages pour créer de nouveaux messages. Les applications clientes le font lorsque les utilisateurs composent un message. Lepooler MAPI le fait lorsqu’il reçoit un message entrant. Dans les deux cas, le nouveau message est généralement créé dans le dossier Boîte de réception de la boutique de messages, s’il en existe un.
  
Les fournisseurs de magasins de messages utilisent beaucoup les tables, dossiers, messages et propriétés MAPI. Les détails d’implémentation de ces objets sont documentés dans les tableaux [MAPI,](mapi-tables.md)les [dossiers MAPI,](mapi-folders.md)les [messages MAPI](mapi-messages.md)et la vue d’ensemble de la propriété [MAPI.](mapi-property-overview.md) Vous devez vous familiariser avec ce document avant d’essayer d’implémenter un fournisseur de magasins de messages.
  
Il existe deux types importants de fournisseurs de magasins de messages : ceux qui peuvent agir en tant que magasin de messages par défaut d’un utilisateur et ceux qui ne le peuvent pas. Une magasin de messages par défaut est celle dans laquelle les applications clientes et lepooler MAPI peuvent effectuer n’importe quelle tâche de messagerie, telle que la réception de messages ou la création de dossiers. Un fournisseur de magasin de messages par défaut doit prendre en charge plusieurs fonctionnalités supplémentaires que le nombre minimal requis pour tous les fournisseurs de magasins de messages.
  
## <a name="see-also"></a>Voir aussi

- [Concepts MAPI](mapi-concepts.md)


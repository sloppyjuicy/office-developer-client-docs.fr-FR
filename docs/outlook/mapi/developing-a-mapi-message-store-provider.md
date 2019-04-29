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
  
Comme les autres fournisseurs de services MAPI, les banques de messages sont des bibliothèques de liens dynamiques (dll) qui présentent les services d'un mécanisme de stockage sous-jacent aux applications clientes MAPI et au spouleur MAPI. Le fournisseur de banque de messages présente le mécanisme de stockage sous la forme d'un ensemble hiérarchique de dossiers et de messages que les clients MAPI et le spouleur MAPI peuvent utiliser.
  
L'illustration suivante montre l'architecture de base des messages MAPI de base.
  
**Architecture de banque de messages**
  
![Architecture] de la Banque de messages (media/storearc.gif "Architecture") de la Banque de messages
  
Vous pouvez implémenter un fournisseur de banque de messages à l'aide de n'importe quel type de mécanisme de stockage sous-jacent de votre choix. Toutefois, vous devez tenir compte des problèmes de performances. En outre, le mécanisme de stockage sous-jacent doit être présenté sous la forme d'une collection hiérarchique d'objets MAPI. Ces exigences signifient que les banques de messages sont généralement implémentées à l'aide d'un produit de base de données existant qui prend en charge le stockage hiérarchique des objets dans la base de données et qui possède une interface de programmation ou une structure de fichiers bien définie. Par exemple, les bases de données Microsoft Office Access, SQL et Oracle peuvent être utilisées comme mécanisme de stockage sous-jacent. Certains produits de base de données disposent de jeux de fonctionnalités qui facilitent l'implémentation des fonctionnalités MAPI, de sorte que votre choix de produit de base de données peut être affecté par les fonctionnalités que votre fournisseur de banque de messages doit prendre en charge.
  
L'utilisation d'une base de données existante comme mécanisme de stockage sous-jacent vous permet d'économiser du travail, car il est généralement plus facile de présenter des objets de base de données à des clients MAPI que d'implémenter votre propre mécanisme de stockage hiérarchique. Cette opération vous permet de traiter les opérations MAPI à un niveau plus élevé que si vous implémentez votre propre mécanisme de stockage hiérarchique. Par exemple, la recherche d'un message avec une ligne d'objet particulière devient une question assez simple de création et d'envoi d'une requête de base de données appropriée, plutôt que d'implémenter des routines complexes pour effectuer une recherche dans votre mécanisme de stockage hiérarchique.
  
Les fournisseurs de banques de messages communiquent avec les clients MAPI et le spouleur MAPI pour effectuer des opérations sur des dossiers et des objets. Le fournisseur de banque de messages traduit ces opérations en opérations de niveau inférieur sur le mécanisme de stockage sous-jacent. Le spouleur MAPI communique généralement avec le fournisseur de banque de messages lors de l'envoi et de la réception des messages. Les clients MAPI communiquent généralement avec des fournisseurs de banques de messages pour manipuler la hiérarchie de dossiers et pour lire, modifier, supprimer et envoyer des messages.
  
Le spouleur MAPI et les clients MAPI communiquent avec le fournisseur de banque de messages pour créer de nouveaux messages. Les applications clientes effectuent cette opération lorsque les utilisateurs composent un message. Le spouleur MAPI effectue cette opération lorsqu'il reçoit un message entrant. Dans les deux cas, le nouveau message est généralement créé dans le dossier boîte de réception de la Banque de messages, s'il en existe un.
  
Les fournisseurs de banques de messages utilisent intensivement les tables, les dossiers, les messages et les propriétés MAPI. Les détails de l'implémentation de ces objets sont documentés dans les [tableaux MAPI](mapi-tables.md), les [dossiers MAPI](mapi-folders.md), [les messages MAPI](mapi-messages.md)et la [vue d'ensemble des propriétés MAPI](mapi-property-overview.md). Vous devez vous familiariser avec cette documentation avant de tenter d'implémenter un fournisseur de banque de messages.
  
Il existe deux types importants de fournisseurs de banques de messages: ceux qui peuvent agir comme banque de messages par défaut d'un utilisateur et ceux qui ne le sont pas. Une banque de messages par défaut est une banque dans laquelle les applications clientes et le spouleur MAPI peuvent effectuer n'importe quelle tâche de messagerie, telle que la réception de messages ou la création de dossiers. Un fournisseur de banque de messages par défaut doit prendre en charge plusieurs fonctionnalités supplémentaires par rapport au nombre minimal requis pour tous les fournisseurs de banques de messages.
  
## <a name="see-also"></a>Voir aussi

- [Concepts MAPI](mapi-concepts.md)


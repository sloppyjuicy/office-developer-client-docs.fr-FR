---
title: Hiérarchie d’imbrication MAPI objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6350202eb22edc478f7738bebf6d7f0bc4684ee0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566242"
---
# <a name="mapi-object-containment-hierarchy"></a>Hiérarchie d’imbrication MAPI objet
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La relation contenant-contenu entre les objets spécifie les dépendances de certains objets sur d’autres objets pour l’accès. Pour une application cliente, l’accès aux objets particuliers permettant d’accéder à d’autres personnes. Dans certains cas, la relation contenant-contenu entre les objets implémentés par un fournisseur de services suit une hiérarchie logique. Dans les autres cas, il est arbitraire. 
  
Un client doit accéder à un objet de la session MAPI avant de pouvoir utiliser plusieurs autres objets (par exemple, les fournisseurs de services et le carnet d’adresses MAPI).
  
Contention de banque de messages est basée sur la relation hiérarchique entre les objets dans la banque d’informations : la banque de messages d’objet lui-même, des dossiers, des messages et pièces jointes. Logiquement, les pièces jointes sont contenues dans les messages, les messages dans les dossiers et les dossiers dans la banque de messages. La relation contenant-contenu correspond à cette hiérarchie logique. Pour accéder à un message, par exemple, un client doit accéder tout d’abord le dossier dans lequel se trouve le message. Profils et les objets d’état sont des exemples d’une relation de contenance plus arbitraire. Deux de ces objets sont disponibles par le biais de la session. 
  
Avec certains objets, les conteneurs fournissent l’accès uniquement. Pièces jointes et les destinataires sont des exemples d’objets qui dépendent totalement leurs conteneurs. Le seul accès à une pièce jointe ou un destinataire est via le message auquel il appartient. Autres objets ont des chemins d’accès de substitution. Ces objets sont affectés binaires identificateurs, appelés identificateurs d’entrée, par les fournisseurs de services qui les créer. Identificateurs d’entrée peuvent servir à accéder directement à leurs objets permettant aux clients d’ignorer l’arborescence de la relation contenant-contenu. 
  
L’illustration suivante montre la hiérarchie d’imbrication MAPI. La session se trouve en haut de l’arborescence de car il s’agit par le biais de la session qu’un client accède à tous les autres objets. Le niveau suivant inclut la table de banque de messages, un objet table qui répertorie les propriétés pour tous les fournisseurs de banque de messages dans la session en cours et le carnet d’adresses pour fournir l’accès à tous les fournisseurs de carnet d’adresses. Le message banque tableau et adresse carnet de sont utilisés pour accéder aux objets implémentés par les fournisseurs de service en particulier, suivant, dans l’ordre de contenance.
  
**Hiérarchie d’imbrication MAPI**
  
![Hiérarchie de contenance MAPI] (media/amapi_41.gif "Hiérarchie de contenance MAPI")
  
## <a name="see-also"></a>Voir aussi

- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)


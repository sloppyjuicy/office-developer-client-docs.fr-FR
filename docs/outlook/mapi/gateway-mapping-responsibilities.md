---
title: Responsabilités de mappage de passerelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ad5f4e896b748dc0d7495c428af093af57bc7cdd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783391"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilités de mappage de passerelle

**S’applique à**: Outlook 
  
Lorsqu’une passerelle prenant en charge MAPI reçoit un message contenant des propriétés nommées dans un des jeux de propriété spéciale destinée à contenir les propriétés de passerelle-mappables, la passerelle doit être mappé toutes les propriétés du protocole de la destination système de messagerie. Bien que MAPI recommande que passerelles gérer nommées toutes les propriétés dans les jeux de propriétés spéciales, passerelles doivent gérer deux seulement : adresse et le type d’adresse de messagerie. Étant donné que l’adresse de messagerie et les propriétés de type adresse affectent directement la transmission de message, il est fondamental que passerelles prennent en charge le mappage de ces deux propriétés. Étant donné que les clés de recherche se composent de type d’adresse et l’adresse d’un utilisateur, ils doivent également être traduits si possible.
  
Identificateurs d’entrée ne sont pas censés être traités fréquemment. Pour activer le mappage d’un identificateur d’entrée qui provient d’un système de messagerie à un identificateur d’entrée est utilisable par un autre système de messagerie, la passerelle doit être en mesure d’utiliser le format des deux systèmes. Étant donné que la plupart des passerelles ne sont pas conscients de formats identificateur d’entrée, la traduction d’identificateurs d’entrée est rare.
  
Une autre propriété mappable qui n’est pas censée être traduits fréquemment est le nom complet. Passerelles doivent stocker les noms d’affichage et les transmet, mais pas nécessairement les traduire. 
  


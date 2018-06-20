---
title: Obtention et définition de plusieurs propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 150f2a55bff4188c1f692de8276ed869bcf66c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783412"
---
# <a name="getting-and-setting-multiple-properties"></a>Obtention et définition de plusieurs propriétés

**S’applique à**: Outlook 
  
En définissant les propriétés autant que possible avec le moins de nombre d’appels, à distance activité est diminuée et de réduire la surcharge due avec chaque propriété. Bien que les fournisseurs de services tentez de récupérer les propriétés avant d’effectuer un appel de procédure distante pour l’extraction ou de modification, vous pouvez optimiser cette initiative en demandant plusieurs propriétés pour commencer.
  
Par exemple, si vous travaillez avec des listes de routage qui décrivent les destinataires futurs avec des propriétés nommées appartenant à des jeux de propriétés particulière, traiter tous les destinataires avec deux appels. Utilisez un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour récupérer les identificateurs de toutes les propriétés du destinataire et l’autre [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer toutes les valeurs. L’alternative, un appel à **GetIDsFromNames** suivi par un appel à **GetProps** pour chaque destinataire, est beaucoup plus efficace. 
  


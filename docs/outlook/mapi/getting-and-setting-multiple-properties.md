---
title: Obtention et définition de plusieurs propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299376"
---
# <a name="getting-and-setting-multiple-properties"></a>Obtention et définition de plusieurs propriétés

**S’applique à** : Outlook 2013 | Outlook 2016 
  
En obtenant et en définissant autant de propriétés que possible avec le moins de numéros d'appels, l'activité distante est réduite et la charge impliquée pour chaque propriété est réduite. Bien que les fournisseurs de services essaient de collecter les propriétés avant d'effectuer un appel de procédure distante pour la récupération ou la modification, vous pouvez optimiser cet effort en demandant à plusieurs propriétés de commencer par.
  
Par exemple, si vous utilisez des listes de routage qui décrivent des destinataires à venir avec des propriétés nommées appartenant à des jeux de propriétés spécifiques, traitez tous les destinataires avec deux appels. Utilisez un appel à [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour récupérer les identificateurs de toutes les propriétés de destinataire et l'autre appel à [IMAPIProp:: GetProps](imapiprop-getprops.md) pour récupérer toutes les valeurs. L'alternative, un appel à **GetIDsFromNames** , suivi d'un appel à **GetProps** pour chaque destinataire, est bien moins efficace. 
  


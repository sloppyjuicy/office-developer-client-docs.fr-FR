---
title: Obtention et définition de plusieurs propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
ms.openlocfilehash: de6f33de2793f34fb6dc247bb67fbf09623eef85
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368692"
---
# <a name="getting-and-setting-multiple-properties"></a>Obtention et définition de plusieurs propriétés

**S’applique à** : Outlook 2013 | Outlook 2016 
  
En obtenant et en fixant autant de propriétés que possible avec le moins d’appels possible, l’activité à distance est réduite et la surcharge impliquée dans chaque propriété est réduite. Bien que les fournisseurs de services tentent de collecter des propriétés avant d’effectuer un appel de procédure distante pour la récupération ou la modification, vous pouvez optimiser cet effort en demandant plusieurs propriétés pour commencer.
  
Par exemple, si vous travaillez avec des listes de routage qui décrivent les destinataires futurs avec des propriétés nommées appartenant à des jeux de propriétés particuliers, traitez tous les destinataires avec deux appels. Utilisez un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour récupérer les identificateurs de toutes les propriétés du destinataire et l’autre appel à [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer toutes les valeurs. L’alternative, appeler **GetIDsFromNames** suivi d’un appel à **GetProps** pour chaque destinataire, est beaucoup moins efficace. 
  


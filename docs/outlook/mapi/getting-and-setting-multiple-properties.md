---
title: Obtention et définition de plusieurs propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432260"
---
# <a name="getting-and-setting-multiple-properties"></a>Obtention et définition de plusieurs propriétés

**S’applique à** : Outlook 2013 | Outlook 2016 
  
En obtenant et en fixant autant de propriétés que possible avec le moins d’appels possible, l’activité à distance est réduite et la surcharge impliquée dans chaque propriété est réduite. Bien que les fournisseurs de services tentent de collecter des propriétés avant d’effectuer un appel de procédure distante pour la récupération ou la modification, vous pouvez optimiser cet effort en demandant plusieurs propriétés pour commencer.
  
Par exemple, si vous travaillez avec des listes de routage qui décrivent les destinataires futurs avec des propriétés nommées appartenant à des jeux de propriétés particuliers, traitez tous les destinataires avec deux appels. Utilisez un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour récupérer les identificateurs de toutes les propriétés du destinataire et l’autre appel à [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer toutes les valeurs. L’alternative, appeler **GetIDsFromNames** suivi d’un appel à **GetProps** pour chaque destinataire, est beaucoup moins efficace. 
  


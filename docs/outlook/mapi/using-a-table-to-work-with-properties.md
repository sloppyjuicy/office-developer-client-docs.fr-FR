---
title: Utilisation d'une table pour utiliser les propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439911"
---
# <a name="using-a-table-to-work-with-properties"></a>Utilisation d'une table pour utiliser les propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreuses propriétés sont disponibles à la fois à partir des objets qui les prennent en charge et sous forme de colonnes sur les tableaux. Dans la mesure du possible, récupérez ces propriétés via le tableau.
  
Appeler [IMAPITable:: SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés dont votre client a besoin et la [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes de la table. 
  
Ces deux appels sont généralement suffisants pour récupérer suffisamment d'informations à l'utilisateur, et sont souvent suffisants pour le traitement interne nécessaire, en effectuant un appel à **OpenEntry** pour ouvrir l'objet. 
  
Il existe seulement deux exceptions:
  
- Si la taille de la propriété est de plus de 255 octets. L'interface IMAP * * ne peut pas retourner la valeur de propriété entière, au lieu de la tronquer à 255 octets. Réfléchissez bien à ce compromis. Si vous affichez ces données à l'utilisateur, 255 octets peuvent être suffisants pour un champ textuel tel qu'un commentaire. 
    
- Si vous avez besoin d'une propriété spécifique à partir d'une seule ligne dans un tableau. Dans ce cas, il n'est pas nécessaire de créer une table avec des propriétés qui ne seront jamais utilisées. La plupart du temps, vous aurez besoin des mêmes propriétés pour toutes les lignes.
    


---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567474"
---
# <a name="attsentfor"></a>attSentFor

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’attribut **attSentFor** est codée selon les chaînes comptées bout en bout. Le format de **attSentFor** est la suivante : 
  
 **attSentFor**: 
  
> longueur du nom d’affichage du nom d’affichage longueur adresse _adresse de messagerie_
    
 _adresse de messagerie_
  
> adresse de type **:** 
    
Contrairement à d’autres longueur valeurs, la longueur du nom d’affichage et adresse longueur sont des valeurs de 16 bits non signées au lieu d’entiers longs non signés. Elles incluent toujours abandon de caractères null, toutefois. Les chaînes de type et l’adresse dans l’entrée _d’adresse de messagerie_ sont séparés par un caractère littéral (deux-points), tel que « smtp:joe@nowhere.com ». Uniquement la chaîne d’adresse type combinée **:** est terminée.
  


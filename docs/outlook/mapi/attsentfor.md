---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782985"
---
# <a name="attsentfor"></a>attSentFor

  
  
**S’applique à**: Outlook 
  
L’attribut **attSentFor** est codée selon les chaînes comptées bout en bout. Le format de **attSentFor** est la suivante : 
  
 **attSentFor**: 
  
> longueur du nom d’affichage du nom d’affichage longueur adresse _adresse de messagerie_
    
 _adresse de messagerie_
  
> adresse de type **:** 
    
Contrairement à d’autres longueur valeurs, la longueur du nom d’affichage et adresse longueur sont des valeurs de 16 bits non signées au lieu d’entiers longs non signés. Elles incluent toujours abandon de caractères null, toutefois. Les chaînes de type et l’adresse dans l’entrée _d’adresse de messagerie_ sont séparés par un caractère littéral (deux-points), tel que « smtp:joe@nowhere.com ». Uniquement la chaîne d’adresse type combinée **:** est terminée.
  


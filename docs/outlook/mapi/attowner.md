---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782965"
---
# <a name="attowner"></a>attOwner

  
  
**S’applique à**: Outlook 
  
L’attribut **attOwner** est codée selon les chaînes comptées bout en bout. Le format de **attOwner** est la suivante : 
  
 **attOwner**: 
  
> longueur du nom d’affichage du nom d’affichage longueur adresse _adresse de messagerie_
    
 _adresse de messagerie_
  
> adresse de type **:** 
    
Contrairement à d’autres longueur valeurs, la longueur du nom d’affichage et adresse longueur sont des valeurs de 16 bits non signées au lieu d’entiers longs non signés. Elles incluent toujours abandon de caractères null, toutefois. Les chaînes de type et l’adresse dans l’entrée _d’adresse de messagerie_ sont séparés par un caractère littéral (deux-points), tel que « smtp:joe@nowhere.com ». Uniquement la chaîne d’adresse type combinée **:** est terminée.
  
Le mappage des propriétés MAPI à l’attribut **attOwner** dépend de la classe de message du message encodé. 
  


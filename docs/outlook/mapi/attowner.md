---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318423"
---
# <a name="attowner"></a>attOwner

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'attribut **attOwner** est encodé sous la forme de chaînes comptées, de bout en bout. Le format de **attOwner** est le suivant: 
  
 **attOwner**: 
  
> Display-Name-longueur nom d'affichage-adresse de _messagerie_ -longueur adresse
    
 _adresse de messagerie_
  
> type **:** adresse 
    
Contrairement à d'autres valeurs de longueur, la longueur de nom d'affichage et la longueur d'adresse sont des valeurs 16 bits non signées au lieu d'entiers longs non signés. Toutefois, ils incluent toujours des caractères nuls de fin. Les chaînes de type et d'adresse dans l'entrée _email-address_ sont séparées par un signe deux-points (:) caractère, tel que «SMTP:Joe@nowhere.com». Seul le type combiné **:** la chaîne d'adresse est terminée par un caractère null.
  
Le mappage des propriétés MAPI sur l'attribut **attOwner** dépend de la classe de message du message en cours de codage. 
  


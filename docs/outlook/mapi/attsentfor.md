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
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408837"
---
# <a name="attsentfor"></a>attSentFor

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'attribut **attSentFor** est encodé sous la forme de chaînes comptées, de bout en bout. Le format de **attSentFor** est le suivant: 
  
 **attSentFor**: 
  
> Display-Name-longueur nom d'affichage-adresse de _messagerie_ -longueur adresse
    
 _adresse de messagerie_
  
> type **:** adresse 
    
Contrairement à d'autres valeurs de longueur, la longueur de nom d'affichage et la longueur d'adresse sont des valeurs 16 bits non signées au lieu d'entiers longs non signés. Toutefois, ils incluent toujours des caractères nuls de fin. Les chaînes de type et d'adresse dans l'entrée _email-address_ sont séparées par un signe deux-points (:) caractère, tel que «SMTP:Joe@nowhere.com». Seul le type combiné **:** la chaîne d'adresse est terminée par un caractère null.
  


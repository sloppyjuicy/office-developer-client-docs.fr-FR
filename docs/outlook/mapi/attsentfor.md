---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a5ada6b214c29919365be9d92bd0491a6e483595
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462644"
---
# <a name="attsentfor"></a>attSentFor

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
**L’attribut attSentFor** est codé en tant que chaînes comptées mises de bout en bout. Le format de **attSentFor** est le suivant : 
  
 **attSentFor** : 
  
> display-name-length display-name address-length  _email-address_
    
 _email-address_
  
> type **:** address 
    
Contrairement aux autres valeurs de longueur, les longueurs de nom d’affichage et d’adresse sont des valeurs 16 bits non signées au lieu des nombres longs non signés. Toutefois, elles incluent toujours des caractères null de fin. Les chaînes de type et d’adresse dans l’entrée d’adresse de messagerie sont séparées par un _deux-points_ littéral (:) par exemple« smtp:joe@nowhere.com ». Seul le type combiné **:** chaîne d’adresse est terminée par null.
  


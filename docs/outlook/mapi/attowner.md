---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
ms.openlocfilehash: e20838b79ebc9b6358af72033da6ec75337c2ca9
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404368"
---
# <a name="attowner"></a>attOwner

**S’applique à** : Outlook 2013 | Outlook 2016
  
**L’attribut attOwner** est codé en tant que chaînes comptées mises de bout en bout. Le format de **attOwner est** le suivant :
  
 **attOwner** :
  
> display-name-length display-name address-length _email-address_

 _email-address_
  
> type **:** address

Contrairement aux autres valeurs de longueur, les longueurs de nom d’affichage et d’adresse sont des valeurs 16 bits non signées au lieu des nombres longs non signés. Toutefois, elles incluent toujours des caractères null de fin. Les chaînes de type et d’adresse dans l’entrée d’adresse de messagerie sont séparées par un _deux-points_ littéral (:) par exemple « smtp:joe@nowhere.com ». Seul le type combiné **:** chaîne d’adresse est terminée par null.
  
Le mappage des propriétés MAPI à **l’attribut attOwner** dépend de la classe de message du message en cours d’encodage.
  
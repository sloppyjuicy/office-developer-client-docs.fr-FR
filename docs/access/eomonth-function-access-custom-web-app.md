---
title: Fonction EOMonth (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Renvoie le dernier jour du mois avant ou nombre de mois spécifié.
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781805"
---
# <a name="eomonth-function-access-custom-web-app"></a>Fonction EOMonth (accès personnalisé web app)

Renvoie le dernier jour du mois avant ou nombre de mois spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **EOMonth** (*Date*, *NumberOfMonth*) 
  
**EOMonth** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |La date au format Date/heure, ou une représentation sous forme de texte accepté d’une date de début.  <br/> |
| *NumberOfMonth*  <br/> |Nombre représentant le nombre de mois avant ou après la *Date* .  <br/> |
   
## <a name="remarks"></a>Remarques

Si la *Date* n’est pas une date valide, **EOMonth** renvoie une erreur. 
  
Si la *Date* et *NumberOfMonth* aboutissent à une date non valide, **EOMonth** renvoie une erreur. 
  


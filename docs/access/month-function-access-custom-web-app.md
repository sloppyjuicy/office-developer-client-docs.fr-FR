---
title: Month, fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Renvoie un entier représentant le mois de la date spécifiée.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781959"
---
# <a name="month-function-access-custom-web-app"></a>Month, fonction (accès personnalisé web app)

Renvoie un entier représentant le mois de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Mois** (*Date*) 
  
La fonction **Month** contient l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Une expression qui peut être résolue sur une valeur de Date/heure.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Mois** renvoie la même valeur que **DatePart** (mois, date). 
  
Si la *Date* contient uniquement une partie de l’heure, la valeur renvoyée est 1, le mois de base. 
  


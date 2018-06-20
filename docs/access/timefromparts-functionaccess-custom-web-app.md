---
title: Fonction TimeFromParts (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Renvoie une valeur de temps en fonction de composants spécifiés.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781989"
---
# <a name="timefromparts-function-access-custom-web-app"></a>Fonction TimeFromParts (accès personnalisé web app)

Renvoie une valeur de temps en fonction de composants spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **TimeFromParts** (*Heure*, *Minute*, *seconde*) 
  
La fonction **TimeFromParts** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Heure*  <br/> |Expression d’entier spécifiant les heures.  <br/> |
| *Minute*  <br/> |Expression d’entier indiquant les minutes.  <br/> |
| *Seconde*  <br/> |Expression d’entier indiquant les secondes.  <br/> |
   
## <a name="see-also"></a>Voir aussi

 **TimeFromParts** renvoie une valeur d’heure entièrement initialisé. Si les arguments ne sont pas valides, une erreur est générée. Si un des paramètres est null, la valeur null est renvoyée. 
  


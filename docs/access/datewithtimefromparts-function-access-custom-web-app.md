---
title: Fonction DateWithTimeFromParts (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Renvoie une Date et le temps, basées sur une année, le mois, le jour et l’heure.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781784"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Fonction DateWithTimeFromParts (accès personnalisé web app)

Renvoie une Date et le temps, basées sur une année, le mois, le jour et l’heure.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateWithTimeFromParts** (*Année*, *mois*, *jour*, *heure*, *Minute*, *seconde*) 
  
La fonction **DateWithTimeFromParts** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression d’entier spécifiant une année.  <br/> |
| *Mois*  <br/> |Expression d’entier spécifiant un mois.  <br/> |
| *Jour*  <br/> |Expression d’entier spécifiant un jour.  <br/> |
| *Heure*  <br/> |Expression d’entier spécifiant les heures.  <br/> |
| *Minute*  <br/> |Expression d’entier indiquant les minutes.  <br/> |
| *Seconde*  <br/> |Expression d’entier indiquant les secondes.  <br/> |
   
## <a name="remarks"></a>Remarques

**DateWithTimeFromParts** renvoie une valeur de Date/heure entièrement initialisée. Si les arguments ne sont pas valides, une erreur est générée. Si les arguments obligatoires sont Null, Null est renvoyée. 
  


---
title: Fonction DateFromParts (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l’année, mois et jour.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781786"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Fonction DateFromParts (accès personnalisé web app)

Renvoie une valeur de date pour l’année, mois et jour.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateFromParts** (*Année*, *mois*, *jour*) 
  
La fonction **DateFromParts** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression d’entier spécifiant une année.  <br/> |
| *Mois*  <br/> |Expression d’entier spécifiant un mois, de 1 à 12.  <br/> |
| *Jour*  <br/> |Expression d’entier spécifiant un jour.  <br/> |
   
## <a name="remarks"></a>Remarques

**DateFromParts** renvoie une valeur de date avec la partie de date définie pour l’année, mois et jour et la partie heure la valeur par défaut. Si les arguments ne sont pas valides, une erreur est générée. Si les arguments obligatoires sont nulles, NULL est renvoyée. 
  
## <a name="example"></a>Exemple

L’expression suivante utilise la fonction **DateFromParts** pour calculer le premier jour du mois en cours. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`




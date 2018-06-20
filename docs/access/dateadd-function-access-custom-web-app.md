---
title: Fonction DateAdd (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Renvoie une date spécifiée avec l’intervalle de numéros spécifié (entier positif ou négatif) est ajouté à une partie de la date spécifiée de la date.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781840"
---
# <a name="dateadd-function-access-custom-web-app"></a>Fonction DateAdd (accès personnalisé web app)

Renvoie une date spécifiée avec l’intervalle de numéros spécifié (entier positif ou négatif) est ajouté à une partie de la date spécifiée de la date.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateAdd** (*DatePart*, *nombre*, *Date*) 
  
La fonction **DateAdd** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |La partie de la *Date* à laquelle un nombre entier est ajouté. Reportez-vous à la section Remarques pour la liste des paramètres valides.  <br/> |
| *Number*  <br/> |Est une expression qui peut être résolue vers un entier qui est ajouté à une *partie* de *Date* . Si vous spécifiez une valeur avec une fraction décimale, la fraction est tronquée.  <br/> |
| *Date*  <br/> |Une expression qui peut être résolue sur une valeur de Date/heure. La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie tous les arguments *DatePart* valides. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**trimestre** <br/> |
|**Mois** <br/> |
|**DAYOFYEAR** <br/> |
|**day** <br/> |
|**semaine** <br/> |
|**heure** <br/> |
|**minute** <br/> |
|**seconde** <br/> |
|**milliseconde** <br/> |
   
## <a name="example"></a>Exemple

L’expression suivante calcule le dernier jour du mois en cours.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

L’expression suivante calcule le dernier jour du mois précédent.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`



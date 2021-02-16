---
title: DateAdd, fonction (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Renvoie une date spécifiée avec l’intervalle de nombre spécifié (nombre total positif ou négatif) ajouté à une partie de date spécifiée de cette date.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423201"
---
# <a name="dateadd-function-access-custom-web-app"></a>DateAdd, fonction (application web personnalisée Access)

Renvoie une date spécifiée avec l’intervalle de nombre spécifié (nombre total positif ou négatif) ajouté à une partie de date spécifiée de cette date.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateAdd** (*DatePart*, *Number*, *Date*) 
  
La **fonction DateAdd** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Partie de  *Date*  à laquelle un nombre d’nombres integer est ajouté. Reportez-vous à la section Remarques pour obtenir la liste des paramètres valides.  <br/> |
| *Number*  <br/> |Est une expression qui peut être résolue en un nombre integer qui est ajouté à un  *datepart*  de  *date*  . Si vous spécifiez une valeur avec une fraction décimale, la fraction est tronquée.  <br/> |
| *Date*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression  *d’argument Date,*  expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie tous les arguments  *DatePart*  valides. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**quarter** <br/> |
|**Mois** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**semaine** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**milliseconde** <br/> |
   
## <a name="example"></a>Exemple

L’expression suivante calcule le dernier jour du mois en cours.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

L’expression suivante calcule le dernier jour du mois précédent.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`



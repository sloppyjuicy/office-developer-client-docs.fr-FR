---
title: Fonction DateAdd (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Retourne une date spécifiée avec l’intervalle de nombre spécifié (entier positif ou négatif) ajouté à une partie de date spécifiée de cette date.
ms.openlocfilehash: c6c2c72ea23b05cdf35fa76f3ea40d25150535be
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893920"
---
# <a name="dateadd-function-access-custom-web-app"></a>Fonction DateAdd (Access custom web app)

Retourne une date spécifiée avec l’intervalle de nombre spécifié (entier positif ou négatif) ajouté à une partie de date spécifiée de cette date.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/online/overview)
  
## <a name="syntax"></a>Syntaxe

**DateAdd** (*DatePart*, *Number*, *Date*)
  
La fonction **DateAdd** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Partie de *Date* à laquelle un nombre entier est ajouté. Reportez-vous à la section Remarques pour obtenir la liste des paramètres valides. |
| *Number*  <br/> |Expression qui peut être résolue en entier ajouté à une *datepart* de *date*. Si vous spécifiez une valeur avec une fraction décimale, la fraction est tronquée. |
| *Date*  <br/> |Expression qui peut être résolue en valeur date/heure. Expression d’argument *Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |

## <a name="remarks"></a>Remarques

Le tableau suivant répertorie tous les arguments *DatePart* valides.
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**Trimestre** <br/> |
|**Mois** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**Semaine** <br/> |
|**Heure** <br/> |
|**Minute** <br/> |
|**Deuxième** <br/> |
|**Milliseconde** <br/> |

## <a name="example"></a>Exemple

L’expression suivante calcule le dernier jour du mois en cours.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

L’expression suivante calcule le dernier jour du mois précédent.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`

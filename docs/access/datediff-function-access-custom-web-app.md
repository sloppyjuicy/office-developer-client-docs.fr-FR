---
title: Fonction DateDiff (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.
ms.openlocfilehash: 8464f28348aec521bac17e8b48ab4e36cb8be2a8
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370721"
---
# <a name="datediff-function-access-custom-web-app"></a>Fonction DateDiff (application web personnalisée Access)

Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**DateDiff** (*DatePart*, *StartDate*, *EndDate*)
  
La **fonction DateDiff** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Est la partie de *StartDate* et *EndDate* qui spécifie le type de limite croisée. Reportez-vous à la section Remarques pour obtenir la liste des paramètres valides. |
| *StartDate*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression *d’argument Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |
| *EndDate*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression *d’argument Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |

## <a name="remarks"></a>Remarques

Le tableau suivant répertorie tous les arguments *DatePart* valides.
  
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

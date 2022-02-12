---
title: Fonction DatePart (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Renvoie une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
ms.openlocfilehash: 547168f56e411d95541b01872bd2548b8ceaf193
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770891"
---
# <a name="datepart-function-access-custom-web-app"></a>Fonction DatePart (application web personnalisée Access)

Renvoie une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**DatePart** (*DatePart*, *Date*)
  
La **fonction DatePart** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Partie de *Date*  (valeur de date ou d’heure) pour laquelle un nombre integer est renvoyé. Reportez-vous à la section Remarques pour obtenir la liste des abréviations valides. |
| *Date*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression *d’argument Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |

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
|**weekday** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**milliseconde** <br/> |

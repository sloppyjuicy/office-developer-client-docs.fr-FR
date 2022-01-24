---
title: Fonction DatePart (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Renvoie une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
ms.openlocfilehash: 52a0d5c69c74626ee91f0ee77aaedafa08c8acd3
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180018"
---
# <a name="datepart-function-access-custom-web-app"></a>Fonction DatePart (application web personnalisée Access)

Renvoie une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**DatePart** (*DatePart*, *Date*)
  
La **fonction DatePart** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Partie de *Date*  (valeur de date ou d’heure) pour laquelle un nombre integer est renvoyé. Reportez-vous à la section Remarques pour obtenir la liste des abréviations valides.  <br/> |
| *Date*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression *d’argument Date,* expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.  <br/> |

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

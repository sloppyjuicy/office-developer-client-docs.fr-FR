---
title: DateDiff, fonction (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.
ms.openlocfilehash: 33db2ae5caa55949d0eac86a2bef7f5049d849f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569763"
---
# <a name="datediff-function-access-custom-web-app"></a>DateDiff, fonction (application web personnalisée Access)

Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas l’ajouter pour le *\<service\> moment. Veuillez essayer à nouveau plus tard.* > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
La **fonction DateDiff** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Est la partie de  *StartDate*  et  *EndDate*  qui spécifie le type de limite croisée. Reportez-vous à la section Remarques pour obtenir la liste des paramètres valides.  <br/> |
| *StartDate*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression  *d’argument Date,*  expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.  <br/> |
| *EndDate*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression  *d’argument Date,*  expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.  <br/> |
   
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
   


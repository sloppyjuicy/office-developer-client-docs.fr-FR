---
title: Fonction DateDiff (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites de la partie de date spécifiée, franchie entre la date de début et la date de fin spécifiées.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280722"
---
# <a name="datediff-function-access-custom-web-app"></a>Fonction DateDiff (application Web personnalisée Access)

Renvoie le nombre de limites de la partie de date spécifiée, franchie entre la date de début et la date de fin spécifiées.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
La fonction **DateDiff** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Est la partie de *StartDate* et *EndDate* qui spécifie le type de la limite franchie. RePortez-vous à la section Remarques pour obtenir la liste des paramètres valides.  <br/> |
| *StartDate*  <br/> |Expression qui peut être résolue en une valeur de date/heure. Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.  <br/> |
| *EndDate*  <br/> |Expression qui peut être résolue en une valeur de date/heure. Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie tous les arguments *DatePart* valides. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**trimestre** <br/> |
|**month** <br/> |
|**DayOfYear** <br/> |
|**day** <br/> |
|**mensuel** <br/> |
|**h/24** <br/> |
|**précédente** <br/> |
|**seconde** <br/> |
|**exprimée** <br/> |
   


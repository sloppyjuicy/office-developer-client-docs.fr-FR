---
title: DateDiff, fonction (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415613"
---
# <a name="datediff-function-access-custom-web-app"></a>DateDiff, fonction (application web personnalisée Access)

Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
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
   


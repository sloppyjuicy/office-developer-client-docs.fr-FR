---
title: Fonction DatePart (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Renvoie une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411434"
---
# <a name="datepart-function-access-custom-web-app"></a>Fonction DatePart (application web personnalisée Access)

Renvoie une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DatePart** (*DatePart*, *Date*) 
  
La **fonction DatePart** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Partie de  *Date*  (valeur de date ou d’heure) pour laquelle un nombre integer est renvoyé. Reportez-vous à la section Remarques pour obtenir la liste des abréviations valides.  <br/> |
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
|**weekday** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**milliseconde** <br/> |
   


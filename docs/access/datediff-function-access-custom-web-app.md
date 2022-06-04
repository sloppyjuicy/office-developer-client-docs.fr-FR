---
title: Fonction DateDiff (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Retourne le nombre de limites de partie de date spécifiées franchies entre la date de début et la date de fin spécifiées.
ms.openlocfilehash: 45ffa738e0459cb68ded803383ddae1219e012ec
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893913"
---
# <a name="datediff-function-access-custom-web-app"></a>Fonction DateDiff (Access custom web app)

Retourne le nombre de limites de partie de date spécifiées franchies entre la date de début et la date de fin spécifiées.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/online/overview)
  
## <a name="syntax"></a>Syntaxe

**DateDiff** (*DatePart*, *StartDate*, *EndDate*)
  
La fonction **DateDiff** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Partie de *StartDate* et *EndDate* qui spécifie le type de limite franchie. Reportez-vous à la section Remarques pour obtenir la liste des paramètres valides. |
| *StartDate*  <br/> |Expression qui peut être résolue en valeur date/heure. Expression d’argument *Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |
| *EndDate*  <br/> |Expression qui peut être résolue en valeur date/heure. Expression d’argument *Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |

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

---
title: Month Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Retourne un entier qui représente le mois de la date spécifiée.
ms.openlocfilehash: 2aef5867cc6d33e3b589b0b5df8acf74dd39c66f
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894746"
---
# <a name="month-function-access-custom-web-app"></a>Month Function (Access custom web app)

Retourne un entier qui représente le mois de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

**Mois** (*date*)
  
La fonction **Month** contient l’argument suivant.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Expression qui peut être résolue en valeur date/heure. |

## <a name="remarks"></a>Remarques

**Month** retourne la même valeur que **DatePart** (mois, date).
  
Si *Date*  ne contient qu’une partie de temps, la valeur de retour est 1, le mois de base.
  
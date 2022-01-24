---
title: Month Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Renvoie un nombre integer qui représente le mois de la date spécifiée.
ms.openlocfilehash: 6679d5e77ed5eb83f5d23c312ea2060495044002
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179591"
---
# <a name="month-function-access-custom-web-app"></a>Month Function (Access custom web app)

Renvoie un nombre integer qui représente le mois de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**Month** (*Date*)
  
La **fonction Month** contient l’argument suivant.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Expression qui peut être résolue en valeur Date/Heure.  <br/> |

## <a name="remarks"></a>Remarques

**Month** renvoie la même valeur que **DatePart** (mois, date).
  
Si *Date*  ne contient qu’une partie de l’heure, la valeur de retour est 1, le mois de base.
  
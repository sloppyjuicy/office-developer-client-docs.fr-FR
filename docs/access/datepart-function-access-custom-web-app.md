---
title: Fonction DatePart (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Retourne une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
ms.openlocfilehash: 009270dff57663f6aa3d56f3f6360bed54ce8386
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893829"
---
# <a name="datepart-function-access-custom-web-app"></a>Fonction DatePart (Access custom web app)

Retourne une valeur numérique qui représente la partie date spécifiée de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/online/overview)
  
## <a name="syntax"></a>Syntaxe

**DatePart** (*DatePart*, *Date*)
  
La fonction **DatePart** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Partie de *Date* (valeur de date ou d’heure) pour laquelle un entier sera retourné. Reportez-vous à la section Notes pour obtenir la liste des abréviations valides. |
| *Date*  <br/> |Expression qui peut être résolue en valeur date/heure. Expression d’argument *Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |

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
|**Semaine** <br/> |
|**Heure** <br/> |
|**Minute** <br/> |
|**Deuxième** <br/> |
|**Milliseconde** <br/> |

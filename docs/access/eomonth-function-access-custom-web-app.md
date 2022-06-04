---
title: Fonction EOMonth (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Retourne le dernier jour du mois précédant ou le nombre spécifié de mois.
ms.openlocfilehash: 47c7bf6ffbd8d4ce78296f43396b6504f90069d8
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894081"
---
# <a name="eomonth-function-access-custom-web-app"></a>Fonction EOMonth (Access custom web app)

Retourne le dernier jour du mois précédant ou le nombre spécifié de mois.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

 **EOMonth** (*Date*, *NumberOfMonth*)
  
**EOMonth** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Date de début au format Date/Heure, ou dans une représentation textuelle acceptée d’une date. |
| *NumberOfMonth*  <br/> |Nombre représentant le nombre de mois avant ou après la *date*. |

## <a name="remarks"></a>Remarques

Si *la date* n’est pas une date valide, **EOMonth** renvoie une erreur.
  
Si *Date* plus *NumberOfMonth* génère une date non valide, **EOMonth** retourne une erreur.
  
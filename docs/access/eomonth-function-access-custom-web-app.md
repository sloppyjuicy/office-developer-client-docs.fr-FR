---
title: EOMonth Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Renvoie le dernier jour du mois avant ou le nombre spécifié de mois.
ms.openlocfilehash: 21e9c8e9f613a1e39ae18d7fe8cdc113ad88c4ca
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370503"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth Function (Access custom web app)

Renvoie le dernier jour du mois avant ou le nombre spécifié de mois.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

 **EOMonth** (*Date*, *NumberOfMonth*)
  
**EOMonth contient** les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Date de début au format Date/Heure ou dans une représentation texte acceptée d’une date. |
| *NumberOfMonth*  <br/> |Nombre représentant le nombre de mois avant ou après la *date*. |

## <a name="remarks"></a>Remarques

Si *Date n’est* pas une date valide, **EOMonth** renvoie une erreur.
  
Si *Date* plus *NumberOfMonth* produit une date non valide, **EOMonth** renvoie une erreur.
  
---
title: Year Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Retourne une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
ms.openlocfilehash: 96e697c1e53a06b4bed7d9de93868afa581bccf7
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894648"
---
# <a name="year-function-access-custom-web-app"></a>Year Function (Access custom web app)

Retourne une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

 **Année** (*Date*)
  
La fonction **Year** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Expression qui peut être résolue en valeur date/heure. Expression d’argument *Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |

## <a name="remarks"></a>Remarques

Les valeurs retournées par les fonctions **Année**, **Mois** et **Jour** sont des valeurs grégorienes, quel que soit le format d’affichage de la valeur de date fournie. Par exemple, si le format d’affichage de la date fournie utilise le calendrier Hijri, les valeurs retournées pour les fonctions **Année**, **Mois** et **Jour** sont associées à la date grégorien équivalente.
  
---
title: Year Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
ms.openlocfilehash: 4d35e41b2952c6272e13bbc66dbbe27e5eb030f3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380031"
---
# <a name="year-function-access-custom-web-app"></a>Year Function (Access custom web app)

Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

 **Year** (*Date*)
  
La **fonction Year** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression *d’argument Date* , expression de colonne, variable définie par l’utilisateur ou littéral de chaîne. |

## <a name="remarks"></a>Remarques

Les valeurs renvoyées par **les fonctions Year**, **Month** et **Day** sont des valeurs grégoriennes, quel que soit le format d’affichage de la valeur de date fournie. Par exemple, si le format d’affichage de la date fournie utilise le calendrier Hijri, les valeurs renvoyées pour les fonctions **Year**, **Month** et **Day** seront des valeurs associées à la date grégorienne équivalente.
  
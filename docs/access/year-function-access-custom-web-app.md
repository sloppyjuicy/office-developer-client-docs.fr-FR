---
title: Year Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
ms.openlocfilehash: dd89dfeb4a424348100bca06e977a5c3c8dc3975
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179514"
---
# <a name="year-function-access-custom-web-app"></a>Year Function (Access custom web app)

Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

 **Year** (*Date*)
  
La **fonction Year** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Expression qui peut être résolue en valeur Date/Heure. Expression *d’argument Date,*  expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.  <br/> |

## <a name="remarks"></a>Remarques

Les valeurs renvoyées par les fonctions **Year**, **Month** et **Day** sont des valeurs grégoriennes, quel que soit le format d’affichage de la valeur de date fournie. Par exemple, si le format d’affichage de la date fournie utilise le calendrier Hijri, les valeurs renvoyées pour les fonctions **Year**, **Month** et **Day** seront des valeurs associées à la date grégorienne équivalente.
  
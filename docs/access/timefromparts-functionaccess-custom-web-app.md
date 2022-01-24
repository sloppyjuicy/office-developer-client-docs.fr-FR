---
title: TimeFromParts Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Renvoie une valeur d’heure basée sur les parties spécifiées.
ms.openlocfilehash: 302584f632d045d7b6dfa94b907ed8abc8debf6e
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179535"
---
# <a name="timefromparts-function-access-custom-web-app"></a>TimeFromParts Function (Access custom web app)

Renvoie une valeur d’heure basée sur les parties spécifiées.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**TimeFromParts** (*Hour*, *Minute*, *Second*)
  
La **fonction TimeFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Hour*  <br/> |Expression de nombres integer spécifiant les heures.  <br/> |
| *Minute*  <br/> |Expression de nombres integer spécifiant les minutes.  <br/> |
| *Second*  <br/> |Expression de nombres integer spécifiant les secondes.  <br/> |

## <a name="see-also"></a>Voir aussi

 **TimeFromParts** renvoie une valeur de temps entièrement initialisée. Si les arguments ne sont pas valides, une erreur se produit. Si l’un des paramètres est null, null est renvoyé.
  
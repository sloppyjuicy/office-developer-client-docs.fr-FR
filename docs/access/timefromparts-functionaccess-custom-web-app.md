---
title: TimeFromParts Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Renvoie une valeur d’heure basée sur les parties spécifiées.
ms.openlocfilehash: 3e67a0bd5e148b0c0e0e2f31fb6e932ea96efa6a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776787"
---
# <a name="timefromparts-function-access-custom-web-app"></a>TimeFromParts Function (Access custom web app)

Renvoie une valeur d’heure basée sur les parties spécifiées.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**TimeFromParts** (*Heure*, *Minute*, *Seconde*)
  
La **fonction TimeFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Hour*  <br/> |Expression de nombres integer spécifiant les heures. |
| *Minute*  <br/> |Expression de nombres integer spécifiant les minutes. |
| *Second*  <br/> |Expression de nombres integer spécifiant les secondes. |

## <a name="see-also"></a>Voir aussi

 **TimeFromParts** renvoie une valeur de temps entièrement initialisée. Si les arguments ne sont pas valides, une erreur se produit. Si l’un des paramètres est null, null est renvoyé.
  
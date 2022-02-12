---
title: Fonction Coalesce (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Renvoie la première expression qui n’est pas NULL à partir d’une liste d’arguments.
ms.openlocfilehash: 0f067224b6b447c22313730b3a8a2dfbdd75b1b3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777879"
---
# <a name="coalesce-function-access-custom-web-app"></a>Fonction Coalesce (application web personnalisée Access)

Renvoie la première expression qui n’est pas NULL à partir d’une liste d’arguments.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**Coalesce** (*Value*, [*Value*], ...,[*Value*])
  
La **fonction Coalesce** contient les arguments suivants :
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Valeur*  <br/> |Expression. |

## <a name="remarks"></a>Remarques

Si tous les arguments sont NULL, **Coalesce** renvoie NULL.
  
## <a name="example"></a>Exemple

L’expression suivante est utilisée comme règle de validation pour une table. L’expression garantit que les entrées sont entrées dans les champs Prénom, Nom, Courrier électronique, Mobile Téléphone, Téléphone de travail, Famille Téléphone et Société avant qu’un enregistrement ne soit engagé. Si l’un des champs répertoriés est laissé vide, la fonction **Coalesce** renvoie la valeur Null, ce qui enfreint la règle de validation.
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```

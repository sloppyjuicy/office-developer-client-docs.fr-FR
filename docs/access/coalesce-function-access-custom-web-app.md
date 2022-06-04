---
title: Fonction Coalesce (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Retourne la première expression qui n’est pas NULL à partir d’une liste d’arguments.
ms.openlocfilehash: 4ce14eecd34c781187db4c0aeacb65b6c8075f5a
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893668"
---
# <a name="coalesce-function-access-custom-web-app"></a>Fonction Coalesce (Access custom web app)

Retourne la première expression qui n’est pas NULL à partir d’une liste d’arguments.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/online/overview)
  
## <a name="syntax"></a>Syntaxe

**Coalesce** (*Value*, [*Value*], ...,[*Value*])
  
La fonction **Coalesce** contient les arguments suivants
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Valeur*  <br/> |Expression. |

## <a name="remarks"></a>Remarques

Si tous les arguments sont NULL, **Coalesce** retourne NULL.
  
## <a name="example"></a>Exemple

L’expression suivante est utilisée comme règle de validation pour une table. L’expression garantit que les entrées sont effectuées dans les champs Prénom, Nom, E-mail, Téléphone mobile, Téléphone professionnel, Téléphone personnel et Entreprise avant qu’un enregistrement ne soit validé. Si l’un des champs répertoriés est laissé vide, la fonction **Coalesce** retourne null, ce qui viole la règle de validation.
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```

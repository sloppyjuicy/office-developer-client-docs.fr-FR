---
title: Fonction Coalesce (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Renvoie la première expression qui n’est pas NULL à partir d’une liste d’arguments.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411392"
---
# <a name="coalesce-function-access-custom-web-app"></a>Fonction Coalesce (application web personnalisée Access)

Renvoie la première expression qui n’est pas NULL à partir d’une liste d’arguments.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**Coalesce** (*Value*, [*Value*], ...,[*Value*]) 
  
La **fonction Coalesce** contient les arguments suivants : 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Valeur*  <br/> |Expression.  <br/> |
   
## <a name="remarks"></a>Remarques

Si tous les arguments sont NULL, **Coalesce** renvoie la valeur NULL. 
  
## <a name="example"></a>Exemple

L’expression suivante est utilisée comme règle de validation pour une table. L’expression garantit que les entrées sont entrées dans les champs Prénom, Nom, Courrier électronique, Mobile Téléphone, Téléphone de travail, Famille Téléphone et Société avant qu’un enregistrement ne soit engagé. Si l’un des champs répertoriés est laissé vide, la fonction **Coalesce** renvoie la valeur Null, ce qui enfreint la règle de validation. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```



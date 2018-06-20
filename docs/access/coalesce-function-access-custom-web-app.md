---
title: Fusion de fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Renvoie la première expression n’est pas NULL à partir d’une liste d’arguments.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781824"
---
# <a name="coalesce-function-access-custom-web-app"></a>Fusion de fonction (accès personnalisé web app)

Renvoie la première expression n’est pas NULL à partir d’une liste d’arguments.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**Fusion** (*Valeur*, [*valeur*],..., [*valeur*]) 
  
La fonction de **fusion** contient les arguments suivants 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Valeur*  <br/> |Une expression.  <br/> |
   
## <a name="remarks"></a>Remarques

Si tous les arguments sont NULL, **fusion** renvoie la valeur NULL. 
  
## <a name="example"></a>Exemple

L’expression suivante est utilisée en tant que la règle de validation pour une table. L’expression garantit que les entrées sont effectuées dans les champs Prénom, dernier nom, courrier électronique, téléphone Mobile, travail, accueil téléphone, et compagnie de téléphone avant d’un enregistrement est validé. Si un des champs répertoriés sont vides, la fonction de **fusion** renvoie la valeur Null, ce qui enfreint la règle de validation. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```



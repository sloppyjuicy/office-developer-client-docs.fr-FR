---
title: Fonction DateFromParts (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.
ms.openlocfilehash: f755d686d4a04da8d4c434e937e16c03c11219a4
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179731"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Fonction DateFromParts (application web personnalisée Access)

Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**DateFromParts** (*Year*, *Month*, *Day*)
  
La **fonction DateFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression de nombres integer spécifiant une année.  <br/> |
| *Month*  <br/> |Expression de nombres integer spécifiant un mois, de 1 à 12.  <br/> |
| *Day*  <br/> |Expression de nombres integer spécifiant un jour.  <br/> |

## <a name="remarks"></a>Remarques

**DateFromParts** renvoie une valeur de date avec la partie date définie sur l’année, le mois et le jour spécifiés, et la partie heure définie sur la valeur par défaut. Si les arguments ne sont pas valides, une erreur se produit. Si les arguments obligatoires sont null, la valeur NULL est renvoyée.
  
## <a name="example"></a>Exemple

L’expression suivante utilise **la fonction DateFromParts** pour calculer le premier jour du mois en cours.
  
`DateFromParts(Year(Today()),Month(Today()),1)`

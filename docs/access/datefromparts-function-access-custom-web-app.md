---
title: Fonction DateFromParts (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.
ms.openlocfilehash: f8ab7b0eaed1fbf8b23af8ea9ea8c2450c4cd056
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777809"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Fonction DateFromParts (application web personnalisée Access)

Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**DateFromParts** (*Année*, *Mois*, *Jour*)
  
La **fonction DateFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression de nombres integer spécifiant une année. |
| *Month*  <br/> |Expression de nombres integer spécifiant un mois, de 1 à 12. |
| *Day*  <br/> |Expression de nombres integer spécifiant un jour. |

## <a name="remarks"></a>Remarques

**DateFromParts** renvoie une valeur de date avec la partie date définie sur l’année, le mois et le jour spécifiés, et la partie heure définie sur la valeur par défaut. Si les arguments ne sont pas valides, une erreur se produit. Si les arguments obligatoires sont null, la valeur NULL est renvoyée.
  
## <a name="example"></a>Exemple

L’expression suivante utilise **la fonction DateFromParts** pour calculer le premier jour du mois en cours.
  
`DateFromParts(Year(Today()),Month(Today()),1)`

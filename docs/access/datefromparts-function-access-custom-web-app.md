---
title: Fonction DateFromParts (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.
ms.openlocfilehash: 95839aab8bab46d833e46ef4a33b0f8d0b8ae50c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586452"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Fonction DateFromParts (application web personnalisée Access)

Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas l’ajouter pour le *\<service\> moment. Veuillez essayer à nouveau plus tard.* > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
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




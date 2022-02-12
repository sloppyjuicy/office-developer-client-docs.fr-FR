---
title: Fonction DateWithTimeFromParts (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.
ms.openlocfilehash: 0c45b8581bdd767f161681c5a27c20d07ec68d35
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777816"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Fonction DateWithTimeFromParts (application web personnalisée Access)

Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**DateWithTimeFromParts** (*année*, *mois*, *jour*, *heure*, *minute*, *seconde*)
  
La **fonction DateWithTimeFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression de nombres integer spécifiant une année. |
| *Month*  <br/> |Expression de nombres integer spécifiant un mois. |
| *Day*  <br/> |Expression de nombres integer spécifiant un jour. |
| *Hour*  <br/> |Expression de nombres integer spécifiant les heures. |
| *Minute*  <br/> |Expression de nombres integer spécifiant les minutes. |
| *Second*  <br/> |Expression de nombres integer spécifiant les secondes. |

## <a name="remarks"></a>Remarques

**DateWithTimeFromParts** renvoie une valeur Date/Heure entièrement initialisée. Si les arguments ne sont pas valides, une erreur se produit. Si les arguments obligatoires sont Null, null est renvoyé.
  
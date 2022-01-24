---
title: Fonction DateWithTimeFromParts (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.
ms.openlocfilehash: bd8b2145962b275e9717f2894224685413414398
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180011"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Fonction DateWithTimeFromParts (application web personnalisée Access)

Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)
  
La **fonction DateWithTimeFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression de nombres integer spécifiant une année.  <br/> |
| *Month*  <br/> |Expression de nombres integer spécifiant un mois.  <br/> |
| *Day*  <br/> |Expression de nombres integer spécifiant un jour.  <br/> |
| *Hour*  <br/> |Expression de nombres integer spécifiant les heures.  <br/> |
| *Minute*  <br/> |Expression de nombres integer spécifiant les minutes.  <br/> |
| *Second*  <br/> |Expression de nombres integer spécifiant les secondes.  <br/> |

## <a name="remarks"></a>Remarques

**DateWithTimeFromParts** renvoie une valeur Date/Heure entièrement initialisée. Si les arguments ne sont pas valides, une erreur se produit. Si les arguments obligatoires sont Null, null est renvoyé.
  
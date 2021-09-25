---
title: BETWEEN (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Spécifie une plage à tester.
ms.openlocfilehash: 85fea11c3cf658ef6b5f821cd54304c64aa06743
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562880"
---
# <a name="between-access-custom-web-app"></a>BETWEEN (Application web personnalisée Access)

Spécifie une plage à tester.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *test_expression*  [ PAS ] **ENTRE** *begin_expression* **ET** *end_expression* 
  
**L’opérateur Between** contient les arguments suivants. 
  
|**Argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Oui  <br/> |Expression à tester dans la plage définie par begin_expression  *et*  *end_expression*  . Doit être le même type de données que begin_expression  *et*  *end_expression*  .  <br/> |
| *NOT*  <br/> |Non  <br/> |Spécifie que le résultat du prédicat doit être annulé.  <br/> |
| *begin_expression*  <br/> |Oui  <br/> |Expression valide. Doit être le même type de données que les  *test_expression*  et  *end_expression*  .  <br/> |
| *end_expression*  <br/> |Oui  <br/> |Expression valide. Doit être le même type de données que test_expression  *et*  *begin_expression*  .  <br/> |
| *AND*  <br/> |Oui  <br/> |Indique  *test_expression*  doit se trouve dans la plage indiquée par les begin_expression  *et*  *end_expression*  .  <br/> |
   
## <a name="result-type"></a>Type de résultat

 **Boolean**
  
## <a name="remarks"></a>Remarques

 **Between** renvoie **TRUE** si la valeur de  *test_expression*  est supérieure ou égale à la valeur de  *begin_expression*  et inférieure ou égale à la valeur de  *end_expression*  . 
  
 **NOT BETWEEN renvoie** **TRUE** si la valeur de *test_expression* est  inférieure à la valeur de begin_expression ou supérieure à la valeur de *end_expression* . 
  
Pour spécifier une plage exclusive, utilisez les plages supérieure ( \> ) et inférieure aux opérateurs ( \< ).
  


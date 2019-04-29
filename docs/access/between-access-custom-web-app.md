---
title: ENTRE (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Spécifie une plage à tester.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429298"
---
# <a name="between-access-custom-web-app"></a>ENTRE (application Web personnalisée Access)

Spécifie une plage à tester.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *test_expression*  AUCUN **Entre** *début_expression* **Et** *fin_expression* 
  
L'opérateur **between** contient les arguments suivants. 
  
|**Argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Oui  <br/> |Expression à tester dans la plage définie par les valeurs *début_expression* et *fin_expression* . Doit être du même type de données que *début_expression* et *fin_expression* .  <br/> |
| *NOT*  <br/> |Non  <br/> |Spécifie que le résultat du prédicat doit être inversé.  <br/> |
| *début_expression*  <br/> |Oui  <br/> |Expression valide. Doit être le même type de données que *test_expression* et *fin_expression* .  <br/> |
| *fin_expression*  <br/> |Oui  <br/> |Expression valide. Doit être le même type de données que *test_expression* et *début_expression* .  <br/> |
| *AND*  <br/> |Oui  <br/> |Indique que *test_expression* doit être compris dans la plage indiquée par *début_expression* et *fin_expression* .  <br/> |
   
## <a name="result-type"></a>Type de résultat

 **Boolean**
  
## <a name="remarks"></a>Remarques

 **Between** renvoie **true** si la valeur de *test_expression* est supérieure ou égale à la valeur de *début_expression* et inférieure ou égale à la valeur de *fin_expression* . 
  
 **Not between** renvoie **true** si la valeur de *test_expression* est inférieure à la valeur de *début_expression* ou supérieure à celle de *fin_expression* . 
  
Pour spécifier une plage exclusive, utilisez les opérateurs supérieur à\>() et inférieur à (\<).
  


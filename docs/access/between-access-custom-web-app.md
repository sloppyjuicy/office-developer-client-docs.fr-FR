---
title: ENTRE (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Spécifie une plage à tester.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781826"
---
# <a name="between-access-custom-web-app"></a>ENTRE (accès personnalisé web app)

Spécifie une plage à tester.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *test_expression*  [NOT] **BETWEEN** *begin_expression* **Et** *fin_expression* 
  
L’opérateur **Between** contient les arguments suivants. 
  
|**Argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Oui  <br/> |Expression à tester dans la plage définie par les *paramètres début_expression* et *fin_expression* . Doit être du même type que *début_expression* et *fin_expression* .  <br/> |
| *NOT*  <br/> |Non  <br/> |Spécifie que le résultat du prédicat est inversée.  <br/> |
| *begin_expression*  <br/> |Oui  <br/> |Une expression valide. Doit être le même type de données que *test_expression* et *fin_expression* .  <br/> |
| *fin_expression*  <br/> |Oui  <br/> |Une expression valide. Doit être du même type que *test_expression* et *début_expression* .  <br/> |
| *AND*  <br/> |Oui  <br/> |Indique que *test_expression* doit se trouver dans la plage indiquée par les *paramètres début_expression* et *fin_expression* .  <br/> |
   
## <a name="result-type"></a>Type de résultat

 **Booléen**
  
## <a name="remarks"></a>Notes

 **BETWEEN** renvoie **la valeur TRUE** si la valeur de *test_expression* est supérieure ou égale à celle de *début_expression* et inférieure ou égale à celle de *fin_expression* . 
  
 **NOT BETWEEN** renvoie **la valeur TRUE** si la valeur de *test_expression* est inférieure à celle de *début_expression* ou supérieure à celle de *fin_expression* . 
  
Pour spécifier un intervalle exclusif, utilisez la plus grande que (\>) et inférieur à opérateurs (\<).
  


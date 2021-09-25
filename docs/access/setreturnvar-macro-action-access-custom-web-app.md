---
title: SetReturnVar Macro action (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: L’action SetReturnVar crée une variable de retour et la définit sur une valeur spécifique.
ms.openlocfilehash: 0560ec9b1d4adbe215e5c187bcc1135c605b3ee9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614744"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar Macro action (Access custom web app)

**L’action SetReturnVar** crée une variable de retour et la définit sur une valeur spécifique. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> **L’action SetReturnVar** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Paramètre

**L’action SetReturnVar** possède les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| _Name_ <br/> |Oui  <br/> |Chaîne qui spécifie le nom de la variable.  <br/> |
| _Expression_ <br/> |Oui  <br/> |Expression destiné à être utilisé pour définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression d’un signe égal (=). Vous pouvez cliquer sur le bouton **Générer** afin d’utiliser le **Générateur d’expressions** pour définir cet argument.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’action SetReturnVar** est utilisée pour créer une variable **ReturnVar**, qui peut être utilisée par les macros qui appellent une macro de données à l’aide de l’action **ExécuterMacroDonnées.** 
  
Une fois **qu’unevar** de retour est créée par l’action **SetReturnVar,** la macro appelant peut l’utiliser dans une expression. Par exemple, si vous avez créé une variable **ReturnVar** nommée **UpdateSuccess,** vous pouvez utiliser la variable à l’aide de la syntaxe suivante :
  
`=[ReturnVars]![UpdateSuccess]`

**L’action SetReturnVar** ne peut être utilisée que dans les macros de données nommées. Elle n’est pas disponible dans les macros de données attachées à un événement de macro de données. 
  


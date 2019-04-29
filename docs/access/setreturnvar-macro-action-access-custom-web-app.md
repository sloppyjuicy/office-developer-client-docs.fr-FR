---
title: SetReturnVar, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: L'action SetReturnVar crée une variable de retour et lui affecte une valeur spécifique.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409593"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar, action de macro (application Web personnalisée Access)

L'action **SetReturnVar** crée une variable de retour et lui affecte une valeur spécifique. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> L'action **SetReturnVar** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Setting

L'action **SetReturnVar** utilise les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| _Nom_ <br/> |Oui  <br/> |Chaîne qui spécifie le nom de la variable.  <br/> |
| _Expression_ <br/> |Oui  <br/> |Expression destiné à être utilisé pour définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression d’un signe égal (=). Vous pouvez cliquer sur le bouton **Générer** afin d’utiliser le **Générateur d’expressions** pour définir cet argument.  <br/> |
   
## <a name="remarks"></a>Remarques

L'action **SetReturnVar** est utilisée pour créer une **ReturnVar**, variable qui peut être utilisée par les macros qui appellent une macro de données à l'aide de l'action **RunDataMacro** . 
  
Une fois qu'une **ReturnVar** a été créée par l'action **SetReturnVar** , la macro appelante peut l'utiliser dans une expression. Par exemple, si vous avez créé un **ReturnVar** nommé **UpdateSuccess**, vous pouvez utiliser la variable à l'aide de la syntaxe suivante:
  
`=[ReturnVars]![UpdateSuccess]`

L'action **SetReturnVar** peut être utilisée uniquement dans les macros de données nommées. Elle n'est pas disponible dans les macros de données qui sont attachées à un événement de macro de données. 
  


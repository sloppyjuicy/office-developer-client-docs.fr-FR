---
title: Action de SetReturnVar Macro (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: L’action SetReturnVar crée une variable de renvoi et lui affecte une valeur spécifique.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782004"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>Action de SetReturnVar Macro (accès personnalisé web app)

L’action **SetReturnVar** crée une variable de renvoi et lui affecte une valeur spécifique. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> L’action **SetReturnVar** est disponible uniquement dans les Macros de données. 
  
## <a name="setting"></a>Valeur

L’action **SetReturnVar** possède les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| _Name_ <br/> |Oui  <br/> |Chaîne qui spécifie le nom de la variable.  <br/> |
| _Expression_ <br/> |Oui  <br/> |Une expression qui sera utilisée pour définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression avec le signe égal (=). Vous pouvez cliquer sur le bouton **Générer** pour utiliser le **Générateur d’Expression** pour définir cet argument.  <br/> |
   
## <a name="remarks"></a>Remarques

L’action **SetReturnVar** est utilisée pour créer un **ReturnVar**, qui est la variable peut être utilisé par des macros qui appeler une macro de données à l’aide de l’action **ExécuterMacroDonnées** . 
  
Une fois un **ReturnVar** est créé par l’action **SetReturnVar** , la macro appelante peut l’utiliser dans une expression. Par exemple, si vous avez créé un **ReturnVar** nommé **UpdateSuccess**, vous pouvez utiliser la variable à l’aide de la syntaxe suivante :
  
`=[ReturnVars]![UpdateSuccess]`

L’action **SetReturnVar** peut être utilisée uniquement dans les macros de données nommée. Il n’est pas disponible dans les macros de données associées à un événement de macro de données. 
  


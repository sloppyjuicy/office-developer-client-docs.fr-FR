---
title: RUNADDON, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Exécute un module complémentaire ou une macro dans un Microsoft projet Visual Basic pour Applications (VBA).
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789589"
---
# <a name="runaddon-function"></a>RUNADDON, fonction

Exécute un module complémentaire ou une macro dans un Microsoft projet Visual Basic pour Applications (VBA). 
  
## <a name="syntax"></a>Syntaxe

RUNADDON (« *chaîne* ») 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Le nom d’un module complémentaire de la collection **Addons** ou d’une macro dans un projet VBA.  <br/> |
   
## <a name="remarks"></a>Remarques

Si le projet du document qui contient l’appel de fonction RUNADDON (ou un autre projet s’il est référencé) n’a pas de macro (une procédure sans argument) nommée _chaîne_, Microsoft Visio exécute le module complémentaire nommé _chaîne_. Si aucun module complémentaire nommé _chaîne_ ne peut être trouvé, Visio ne fait rien et ne génère aucune erreur. (Vous pouvez utiliser la propriété **TraceFlags** pour contrôler les procédures et les modules complémentaires Visio tente de s’exécuter). 
  
Lorsque vous appelez une procédure dans un module standard, il est recommandé de préfixe de la chaîne avec le nom du module qui contient la procédure (par exemple, *moduleName.procName*), car plusieurs modules peuvent avoir une procédure portant le même nom. 
  
Pour appeler une procédure dans un projet autre que le projet du document qui contient l’appel de fonction RUNADDON, utilisez la syntaxe *projName.modName.procName* (vous devez avoir explicitement défini une référence au *NomProj* dans votre projet VBA). 
  
> [!NOTE]
>  À partir de Visio 2002, la fonction RUNADDON ne peut exécuter une chaîne contenant du code VBA arbitraire. Le code précédemment transmis à la fonction RUNADDON peut être déplacé vers une procédure dans un projet VBA de document appelé à partir de la fonction RUNADDON. 
  
Pour plus d’informations sur l’exécution de code dans Visio, voir [sur les paramètres de sécurité et l’exécution de Code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDON. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles. 
  
## <a name="example-1"></a>Exemple 1

RUNADDON("Calendar.exe")
  
Lance un module complémentaire appelé Calendar.exe.
  
## <a name="example-2"></a>Exemple 2

RUNADDON("Array Shapes")
  
Lance le module complémentaire (implémenté par VSL) dont le nom est Array Shapes.
  
## <a name="example-3"></a>Exemple 3

RUNADDON("ThisDocument.ReportStatistics")
  
Appelle la macro ReportStatistics dans le module **ThisDocument** dans le projet de document contenant cet appel de fonction. 
  
> [!NOTE]
>  Pour appeler une macro dans le module **ThisDocument** , vous devez faire précéder la chaîne de « ThisDocument » comme indiqué. 
  
## <a name="example-4"></a>Exemple 4

RUNADDON (« *NomModule* . ReportStatistics ») 
  
Appelle la macro ReportStatistics dans *NomModule* dans le projet de document qui contient cet appel de fonction. 
  


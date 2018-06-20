---
title: RUNADDONWARGS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Exécute la chaîne et transmet les arguments de ligne de commande pour le programme sous forme de chaîne.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789585"
---
# <a name="runaddonwargs-function"></a>RUNADDONWARGS, fonction

Exécute la _chaîne_ et transmet les _arguments_ ligne de commande pour le programme sous forme de chaîne. 
  
## <a name="syntax"></a>Syntaxe

RUNADDONWARGS (« ** *chaîne* ** », » ** *arguments* ** ») 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Nom d’un module complémentaire  <br/> |
| _arguments_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Arguments à transmettre à votre programme  <br/> |
   
## <a name="remarks"></a>Remarques

En pratique, _arguments_ doit comporter 50 caractères au maximum. Utilisez la fonction RUNADDONWARGS pour lier un programme, par exemple un module complémentaire, à une cellule, par exemple, à la cellule Action ou Events. 
  
La fonction RUNADDONWARGS peut uniquement exécuter des modules complémentaires qui sont membres de la collection **Addons** de l’application. Pour être présents dans la collection, un module complémentaire doit être un fichier EXE ou VSL qui est : 
  
- Installé dans le chemin d’accès **Startup** ou **Addons** de l’application. 
    
- Ajout par programme à l’aide de la méthode **Add** de la collection **Addons** . 
    
Pour plus d’informations sur l’exécution de code dans Visio, voir [sur les paramètres de sécurité et l’exécution de Code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDONWARGS. Les versions de l’application Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles.
  
## <a name="example"></a>Exemple

RUNADDONWARGS (GRAPHMKR ». EXE », « / GraphMaker = Stack ») 
  
Lance le module complémentaire Graphmkr.exe et lui transmet l’argument /GraphMaker=Stack. 
  


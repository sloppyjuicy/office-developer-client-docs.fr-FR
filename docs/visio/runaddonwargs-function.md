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
description: Exécute une chaîne et transmet les arguments de ligne de commande au programme sous la forme d'une chaîne.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318948"
---
# <a name="runaddonwargs-function"></a>Fonction RUNADDONWARGS

Exécute une _chaîne_ et transmet les _arguments_ de ligne de commande au programme sous la forme d'une chaîne. 
  
## <a name="syntax"></a>Syntaxe

RUNADDONWARGS ("* * *chaîne* * *", "* * *arguments* * *") 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obligatoire  <br/> |**String** <br/> | Nom d’un module complémentaire  <br/> |
| _arguments_ <br/> |Obligatoire  <br/> |**String** <br/> |Arguments à transmettre à votre programme  <br/> |
   
## <a name="remarks"></a>Remarques

En pratique, les _arguments_ doivent être 50 ou moins de caractères. Utilisez la fonction RUNADDONWARGS pour lier un programme, tel qu’un module complémentaire, à une cellule, par exemple à la cellule Action ou Events. 
  
La fonction RUNADDONWARGS ne peut exécuter que des modules complémentaires membres de la collection **Addons** de l’application. Pour faire partie de cette collection, un module complémentaire doit être un fichier EXE ou VSL qui est : 
  
- installé dans le chemin d’accès **Startup** ou **Addons** de l’application ; 
    
- ajouté par programme à l’aide de la méthode **Add** de la collection **Addons**. 
    
Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDONWARGS. Les versions de l’application Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles.
  
## <a name="example"></a>Exemple

RUNADDONWARGS ("GRAPHMKR. EXE ","/GraphMaker = Stack ") 
  
Lance le module complémentaire Graphmkr.exe et lui transmet l’argument /GraphMaker=Stack. 
  


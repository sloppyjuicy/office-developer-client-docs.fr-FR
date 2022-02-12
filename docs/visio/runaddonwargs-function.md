---
title: RUNADDONWARGS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
ms.localizationpriority: medium
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Exécute une chaîne et transmet les arguments de ligne de commande au programme en tant que chaîne.
ms.openlocfilehash: bd0ba6277b6d630d6399ef1af4c28e1d30043bcf
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772661"
---
# <a name="runaddonwargs-function"></a>Fonction RUNADDONWARGS

Exécute  _une_ chaîne et transmet les  _arguments de ligne de commande_ au programme en tant que chaîne. 
  
## <a name="syntax"></a>Syntaxe

RUNADDONWARGS( » ** *string* ** « , » ** *arguments* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Requis  <br/> |**String** <br/> | Nom d’un module complémentaire |
| _arguments_ <br/> |Requis  <br/> |**String** <br/> |Arguments à transmettre à votre programme |
   
## <a name="remarks"></a>Remarques

Dans la pratique,  _les arguments_ doivent avoir 50 caractères ou moins. Utilisez la fonction RUNADDONWARGS pour lier un programme, tel qu’un module complémentaire, à une cellule, par exemple à la cellule Action ou Events. 
  
La fonction RUNADDONWARGS ne peut exécuter que des modules complémentaires membres de la collection **Addons** de l’application. Pour faire partie de cette collection, un module complémentaire doit être un fichier EXE ou VSL qui est : 
  
- installé dans le chemin d’accès **Startup** ou **Addons** de l’application ; 
    
- ajouté par programme à l’aide de la méthode **Add** de la collection **Addons**. 
    
Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDONWARGS. Les versions de l’application Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles.
  
## <a name="example"></a>Exemple

RUNADDONWARGS(« GRAPHMKR.EXE »,"/GraphMaker=Stack ») 
  
Lance le module complémentaire Graphmkr.exe et lui transmet l’argument /GraphMaker=Stack. 
  


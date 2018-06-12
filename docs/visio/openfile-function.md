---
title: OPENFILE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert et Active la fenêtre de document.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789188"
---
# <a name="openfile-function"></a>OPENFILE, fonction

Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert et Active la fenêtre de document.
  
## <a name="syntax"></a>Syntaxe

 **OPENFILE** ( _« filename »_)
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nom de fichier_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Le nom du fichier, y compris le chemin d’accès du fichier, que vous souhaitez ouvrir.  <br/> |
   
## <a name="remarks"></a>Note

Si plusieurs fonctions OPENFILE sont déclenchées, elles sont mises en file d’attente et exécutées dans l’ordre d’évaluation. Si le document Visio ouvert est activé pour une modification à l’écran (dans une autre application), une nouvelle copie de Visio est lancée avec le nom de fichier demandé. 
  
Cette fonction renvoie toujours la valeur FALSE. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _OPENFILE. Les versions Visio 4.0 et ultérieures acceptent les deux styles. 
  
## <a name="example"></a>Exemple

 `OPENFILE("C:/MyFile.vsdx")`
  
Ouvre le fichier « MyFile.vsdx » spécifié dans une nouvelle fenêtre ou Active la fenêtre si le fichier est déjà ouvert. 
  

